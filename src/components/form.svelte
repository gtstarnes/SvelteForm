<script lang="ts">

    let fields = {firstName: '', lastName: '', email: '', phoneNumber: '', password: '', confirmPassword: ''};
    let error = {firstName: '', lastName: '', email: '', phoneNumber: '', password: '', confirmPassword: ''};
    let valid = false;

    const resetForm = () => {
        fields = {firstName: '', lastName: '', email: '', phoneNumber: '', password: '', confirmPassword: ''};
        error = {firstName: '', lastName: '', email: '', phoneNumber: '', password: '', confirmPassword: ''};
    }

    const submitForm = () => {

    }

</script>

<form on:submit|preventDefault={submitForm}>
    <h4>This is not a real online service! You know you need something like this in your life to help you realize your deepest dreams. Sign up <span>now</span> to get started.</h4>
    <h4>You <span>know</span> you want to.</h4>
    <div >
        <h3>Let's do this!</h3>
        <div class="form">
            <div class="form-field">
                <label for="firstname">First Name</label>
                <input id="firstname" name="firstname" type="text" bind:value={fields.firstName} />
                <p class="error">{error.firstName}</p>
            </div>
            <div class="form-field">
                <label for="lastname">Last Name</label>
                <input id="lastname" name="lastname" type="text" bind:value={fields.lastName} />
                <p class="error">{error.lastName}</p>
            </div>
            <div class="form-field">
                <label for="email">Email</label>
                <input id="email" name="email" type="email" bind:value={fields.email} />
                <p class="error">{error.email}</p>
            </div>
            <div class="form-field">
                <label for="phonenumber">Phone Number</label>
                <input id="phonenumber" name="phonenumber" type="tel" bind:value={fields.phoneNumber} />
                <p class="error">{error.phoneNumber}</p>
            </div>
            <div class="form-field">
                <label for="password">Password</label>
                <input id="password" name="password" type="password" bind:value={fields.password} />
                <p class="error">{error.password}</p>
            </div>
            <div class="form-field">
                <label for="confirm">Confirm Password</label>
                <input id="confirm" name="confirm" type="password" bind:value={fields.confirmPassword} />
                <p class="error">{error.confirmPassword}</p>
            </div>
        </div>
    </div>
    <button>Create Account</button>
    <p>Already have an account? <a href="#">Log in</a></p>
</form>

<style>
    button {
        background-color: #596D48;
        width: 26%;
        padding: .8rem;
        outline:inherit;
        border: none;
        border-radius: 2%;
        cursor: pointer
    }    
    form {
        font-family:'Lucida Sans', 'Lucida Sans Regular', 'Lucida Grande', 'Lucida Sans Unicode', Geneva, Verdana, sans-serif;
        padding-left: 6%;
    }
    .form {
        display: grid;
        grid-template-columns: 30% 30%;
        column-gap: 3rem;
        background-color: grey;
        filter:drop-shadow(1px 2px 4px grey)
    }
    .form-field {
        display: flex;
        flex-direction: column;
    }
    h4 {
        max-width: 70%;
    }
    input {
        padding: .5rem
    }
    span {
        font-style: italic;
    }
</style>