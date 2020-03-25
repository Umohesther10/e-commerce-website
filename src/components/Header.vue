<template>
  <div class="head">
    <div>
      <b-navbar toggleable="lg" type="dark" variant="primary" fixed="top">
        <b-navbar-brand style="font-size: 30px" href="/">CHERRY ONLINE SHOP</b-navbar-brand>

        <b-navbar-toggle target="nav-collapse"></b-navbar-toggle>

        <b-collapse id="nav-collapse" is-nav>
          <b-navbar-nav></b-navbar-nav>

          <!-- Right aligned nav items -->
          <b-navbar-nav class="ml-auto">
            <b-nav-form>
              <b-form-input
                style="width: 500px; padding: 20px;"
                size="sm"
                class="mr-sm-2"
                placeholder="Search, Products, Categories"
              ></b-form-input>
              <b-button
                style="border: 1px, solid ; border-radius: 10px;"
                size="sm"
                class="my-2 my-sm-0"
                type="submit"
                variant="primary"
              >Search</b-button>
            </b-nav-form>

            <!-- <b-nav-item-dropdown text="Lang" right>
              <b-dropdown-item href="#">EN</b-dropdown-item>
              <b-dropdown-item href="#">ES</b-dropdown-item>
              <b-dropdown-item href="#">RU</b-dropdown-item>
              <b-dropdown-item href="#">FA</b-dropdown-item>
            </b-nav-item-dropdown>-->

            <b-nav-item-dropdown right>
              <!-- Using 'button-content' slot -->
              <template v-slot:button-content>
                <em>User</em>
              </template>
              <b-dropdown-item href="#">Profile</b-dropdown-item>
              <b-dropdown-item href="#">Sign Up</b-dropdown-item>
              <b-dropdown-item href="#">Cart</b-dropdown-item>
              <b-dropdown-item href="#">Sign Out</b-dropdown-item>
            </b-nav-item-dropdown>
          </b-navbar-nav>
        </b-collapse>
      </b-navbar>
    </div>
  </div>
</template>

<script>
export default {};
</script>

<style>
.head {
  margin-bottom: 20px;
}
</style>
