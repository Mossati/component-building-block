<script>
    let {title, body, job, imgSrc, imgAlt, cardType} = $props();
</script>

<li class={cardType} style="--imgSrc: url('{imgSrc}')">
    <div>
        <img src={imgSrc} alt={imgAlt} width="100" height="100">
    </div>

    <article>
        <span>{job}</span>
        <h2>{title}</h2>
        <p>{body}</p>
    </article>
</li>

<style>
    li {
        padding: 0.5rem;
        background-image: linear-gradient(345deg, rgba(255, 255, 255, 0.75), rgba(255, 255, 255, 1));
        border-radius: 1rem;
        flex : 1;
        display: flex;
        flex-direction: column;
        gap: 0.5rem;
        min-height: 25rem;
        box-shadow: 
        inset 0 0.05rem 0.05rem 0 rgba(255, 255, 255, 0.2),
        0 0.5rem 1rem rgba(0, 0, 0, 0.2);
    }

    h2 {
        background-image: linear-gradient(90deg, var(--background-primary), var(--background-secondary));
        background-clip: text;
        color: transparent;
        font-size: 1.5rem;
    }

    span {
        display: inline-block;
        font-size: 0.875rem;
        border-radius: 1rem;
        background-color: var(--background-primary);
        color: var(--text-secondary);
        padding: 0.25rem 1rem;
    }

    p {
        font-size: 1rem;
        overflow-y: hidden;
    }

    div {
        background-color: var(--background-secondary);
        border-radius: 0.5rem;
        width: 100%;
        height: 10rem;
        overflow: hidden;
    }

    img {
        width: 100%;
        height: auto;
        object-fit: cover;
    }

    .visual-card {
        background-image: var(--imgSrc);
        background-size: cover;
        background-position: center;
        background-repeat: no-repeat;
        flex-direction: unset;
        flex-wrap: wrap;
        place-content: end start;
        padding: 0;
        transition: transform 0.2s ease-out;
    }

    .visual-card:hover {
        animation-name: backgroundZoom;
        animation-duration: 1s;
        animation-fill-mode: forwards;
    }

    @keyframes backgroundZoom {
        0% {
            background-size: cover;
        }
        100% {
            background-size: 250%;
        }
    }

    .visual-card div {
        display: none;
    }

    .visual-card article {
        background-image: linear-gradient(0deg, rgb(0, 79, 89), transparent);
        /* backdrop-filter: blur(0.5rem); */
        border-radius: 0.5rem;
        padding: 0.5rem;
    }

    .visual-card article p {
        color: var(--text-secondary);
    }
</style>