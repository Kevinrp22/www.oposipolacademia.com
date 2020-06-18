<style>
  .form-bienvenida {
    box-sizing: border-box;
    width: 100%;
    padding: 20px;
    background-color: #ffffff;
  }
  .form-bienvenida input {
    padding: 18px 1px 18px 40px;
    width: 100%;
    font-size: 0.8rem;
  }
  .form-bienvenida textarea {
    box-sizing: border-box;
    padding: 15px;
    width: 100%;
    font-size: 0.8rem;
    height: 150px;
    resize: none;
  }
  .c-inputs {
    display: grid;
    grid-template-columns: repeat(1, 1fr);
    gap: 5px 15px;
  }
  .grupo {
    position: relative;
  }
  .grupo span i {
    color: #888888;
  }
  .grupo span {
    display: flex;
    align-items: center;
    position: absolute;
    top: 0;
    bottom: 0;
    left: 15px;
  }
  .form-bienvenida .btn {
    margin-top: 0.5rem;
    width: 100%;
  }

  input,
  textarea {
    color: black;
    letter-spacing: 0px;
    font-family: "Monserrat", sans-serif;
    text-transform: initial;
    font-family: inherit;
    font-size: 0.9em;
    padding: 0.4em;
    box-sizing: border-box;
    border: 1px solid #ccc;
    border-radius: 1px;
  }
</style>

<form action="" class="form-bienvenida">
  <div class="c-inputs">
    <div class="grupo">
      <input type="text" placeholder="Nombre" />
      <span>
        <i class="fas fa-user" />
      </span>
    </div>
    <div class="grupo">
      <input type="text" placeholder="Email (Obligatorio)" required />
      <span>
        <i class="fas fa-envelope" />
      </span>
    </div>
    <div class="grupo">
      <input type="tel" placeholder="Teléfono" />
      <span>
        <i class="fas fa-phone-alt" />
      </span>
    </div>
    <div class="grupo">
      <textarea name="" id="" placeholder="Comentario" />

    </div>
  </div>
  <button class="btn" type="submit">ENVIAR</button>

</form>
