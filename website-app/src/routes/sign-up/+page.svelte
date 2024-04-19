<script>

    import { image5 } from "$lib";

</script>
<style>
    .signup-container {
        max-width: 400px;
        margin: 50px auto;
        background-color: #fff;
        padding: 20px;
        border-radius: 20px;
        box-shadow: 0 0 10px rgba(0.1, 0.1, 0.1, 0.1);
        text-align: center;
    }

    .logo {
        display: flex;
        align-items: center;
        justify-content: center;
        margin-bottom: 20px;
    }

    .logo p {
        margin-left: 10px;
        color: black;
        font-weight: 600;
        font-size: 15px;
        margin-top:10px;
        font-family: 'Segoe UI Emoji';
    }

    p {
        color: #8c8b92;
        font-family: 'Segoe UI';
        font-weight: 400;
    }

    h2 {
        font-weight: 600;
        font-family: 'Segoe UI Emoji';
        font-size: 20px;
        margin-bottom: -10px;
    }

    form {
        display: flex;
        flex-direction: column;
        text-align: center;
    }

    label {
        margin-top: 20px;
        text-align: left;
        margin-left: 40px;
        font-family: 'segoe UI Emoji';
        color: black;
        font-family: 600;
    }

    input {
        margin-left: 40px;
        background-color: white;
        color: black;
        border: 1px solid #ccc;
        border-radius: 4px;
        cursor: pointer;
        margin-top: 10px;
        width: 320px;
        height: 40px;
        font-family: 'segoe-UI';
        font-size: 15px;
        font-weight: 600;
    }

    button {
        background-color: blue;
        color: white;
        padding: 10px;
        border: none;
        border-radius: 4px;
        cursor: pointer;
        margin-top: 30px;
        width: 320px;
        margin-left: 40px;
    }

    .continue-with-google {
        background-color: white;
        color: black;
        border: 1px solid #ccc;
        border-radius: 4px;
        cursor: pointer;
        margin-top: 10px;
        width: 320px;
        height: 45px;
        font-family: 'segoe-UI Emoji';
        font-size: 15px;
        font-weight: 600;
        margin-left: 0px;
    }

    .login-link {
        margin-top: 20px;
        text-align: center;
    }

    .login-link a {
        color: blue;
        text-decoration: none;
    }

    .login-link a:hover {
        text-decoration: underline;
    }
</style>

<body>

    <div class="signup-container">
        <div class="logo">
            <img src= { image5 } alt="Logo">
            <p>Wanderer</p>
        </div>
        <h2>Create your account</h2>
        <p>to continue to Wanderer</p>
        <button class="continue-with-google">Continue with Google</button>
        <form>
            <label for="email">Email address</label>
            <input type="email" id="email" name="email" required>

            <label for="password">Password</label>
            <input type="password" id="password" name="password" required>

            <button type="submit">CONTINUE</button>
        </form>

        <div class="login-link">
            <p>Have an account? <a href="/login">Sign in</a></p>
        </div>
    </div>

</body>
