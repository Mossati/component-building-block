<script>
    import Card from "$lib/component-card.svelte";
</script>

<h1>Component - <span>Card</span></h1>
<ul>
    <Card 
    imgSrc="./ov.jpg"
    imgAlt="public transport"
    job="Manager"
    title="Cash" 
    body="A gross cash amount is paid to you every month. You are expected to manage your own transportation to and from work or client locations. You can use Deloitte-subsidized transport options if desired."/>
    <Card 
    imgSrc="./ov.jpg"
    imgAlt="public transport"
    job="Director"
    title="Mobility +" 
    body="Direct financial compensation is halved. Public transport expenses are fully reimbursed for travel between 9 AM and 5 PM."/>
    <Card 
    cardType="visual-card"
    imgSrc="./lease.jpg"
    imgAlt="lease car"
    job="Director"
    title="Lease Car" 
    body="You receive a lease car provided by Deloitte. Includes access to the Deloitte Business OV Card for public transport as needed."/>
    <Card 
    cardType="visual-card"
    imgSrc="./ov.jpg"
    imgAlt="public transport"
    job="Manager"
    title="Unlimited Public Transport" 
    body="Unlimited access to public transport for work-related travel."/>
</ul>

<style>
    h1 {
        display: inline-block;
        color: var(--text-secondary);
        border-bottom: 0.1rem solid var(--text-secondary);
        margin-bottom: 1rem;
    }

    span {
        font-style: italic;
        font-weight: 200;
        color: var(--text-primary);
    }

    ul {
        list-style-type: "";
        display: flex;
        flex-direction: column;
        justify-content: center;
        align-items: center;
        gap: 1rem;
        background-image: radial-gradient(50% 50% at 50% 50%, rgba(111, 194, 180, 0.5), rgba(111, 194, 180, 0));
    }

    @media only screen and (min-width: 48rem) {
        ul {
            flex-direction: row;
        }
    }
</style>
