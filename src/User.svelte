<style lang="scss">
  @import "../scss/helpers";
  .user {
    display: inline-grid;
    align-items: center;
    grid-template-columns: max-content 50px;
    grid-gap: get-size("300");
  }

  img {
    border-radius: 100%;
  }
</style>

<div class="user">
  <a href="#">My profile</a>
  <img
    src="/images/profile-image.jpg"
    width="50"
    height="50"
    alt="Profile image for Lorem Ipsum" />
</div>
