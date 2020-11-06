<script>
  import {likeCount} from "../store/store"

</script>
<style>
  .Header{
    background-color:white;
    position:fixed;
    width:100%;
  }
  .Header-container{
    display:grid;
    grid-template-columns: minmax(auto, 936px);
    justify-content: center;
    background-color:white;
    border-bottom: 1px solid rgba(38, 38, 38, .4);
  }
  .Header-content{
    display:flex;
    align-items: center;
    justify-content: space-between;
    padding: 0 .5em;
  }
  .Header ul{
    list-style: none;
  }
  .Header li {
    display:inline-block;
    margin:0 0 0 1em;
  }
  .Header i {
    font-size:16px;
    color:rgba(38,38,38, .7);
    cursor:pointer;
  }
  h1{
    padding:0;
    margin:0;
    font-size:28px;
    display: inline-block;
    mix-blend-mode: multiply;
    color: black;
    font-family: "Pacifico", cursive;
    position:relative;
    cursor: pointer;
    background:#fff;
  }
  h1:before{
    content:"";
    width:100%;
    height:100%;
    position: absolute;
    left: 0;
    top: 0;
    mix-blend-mode: screen;
    display:block;
    background: radial-gradient(circle at top left, #f09433, #bc1888); 
     }
</style>
<div class="Header">
  <div class="Header-container">
    <div class="Header-content">
      <div class="Header-logo">
        <h1>Pugstagram</h1>
      </div>
      <div class="Header-nav">
        <ul>
          <li>
            <i class="fas fa-heart" />
            {$likeCount === 0 ? "" : $likeCount}
          </li>
          <li><i class="fas fa-user-alt" /></li>
        </ul>
      </div>
    </div>
  </div>
</div>