<template>
  <div class="container">
    <div class="row">
      <div class="col-md-6 offset-md-3">
        <h2 class="text-center text-dark mt-5">Login</h2>
        <div class="card my-5">
          <form class="card-body cardbody-color p-lg-5">
            <div class="text-center">
              <img
                src="https://i.gyazo.com/7fc4d6acf6588141e3e5cbaca9aff39f.jpg"
                class="
                  img-fluid
                  profile-image-pic
                  img-thumbnail
                  rounded-circle
                  my-3
                "
                width="200px"
                alt="profile"
              />
            </div>

            <div class="mb-3">
              <input
                type="text"
                class="form-control"
                id="Username"
                aria-describedby="emailHelp"
                placeholder="User Name"
              />
            </div>
            <div class="mb-3">
              <input
                type="password"
                class="form-control"
                id="password"
                placeholder="password"
              />
            </div>
            <div class="text-center">
              <button type="submit" class="btn btn-color px-5 mb-5 w-100">
                Login
              </button>
            </div>
            <div id="emailHelp" class="form-text text-center mb-5 text-dark">
              Not Registered?
              <router-link to="/signup" class="text-dark fw-bold">Create an Account</router-link>
            </div>
          </form>
        </div>
      </div>
    </div>
  </div>
</template>

<style scoped>
.btn-color {
  background-color: #0e1c36;
  color: #fff;
}

.profile-image-pic {
  height: 200px;
  width: 200px;
  object-fit: cover;
}
</style>