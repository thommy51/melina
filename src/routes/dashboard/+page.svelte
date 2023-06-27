<div class="container">
    <ul class="sidebar">
        <li><a href="/dashboard" >Dashboard</a></li> 
        <li><a href="/adhoc" >Adhoc</a> </li>
        <li><a href="/inventory" >Inventory</a></li> 
        <li><a href="/dashboard" >Playbooks</a></li> 
        <li><a href="/dashboard" >Plays</a> </li>
        <li><a href="/dashboard" >Tasks</a> </li>
    </ul>
</div>

<style>

    .container{
        height: 100vmin;
    }

    .sidebar{
        height: 100%;
        display: flex;
        align-items: start;
        justify-content: center;
        flex-direction: column;
    }

    .sidebar li{
        list-style: none;
        width: 8em;
        background-color: cadetblue;
        text-align: center;
        border-radius: 10px;
        padding: .4em;
    }

    .sidebar a{
        color: white;
    }

</style>