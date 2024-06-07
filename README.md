   <div className="keypad-container">
      <input type="password" readOnly className="input-display" />
      <div className="keypad">
        {[1, 2, 3].map((num) => (
          <button key={num}>{num}</button>
        ))}
        {[4, 5, 6].map((num) => (
          <button key={num}>{num}</button>
        ))}
        {[7, 8, 9].map((num) => (
          <button key={num}>{num}</button>
        ))}
        <button>CLEAR</button>
        <button>0</button>
        <button className="login-button">LOGIN</button>
      </div>
    </div>
////////////////

.keypad-container {
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  height: 100vh;
}

.input-display {
  width: 200px;
  height: 40px;
  text-align: center;
  margin-bottom: 20px;
  font-size: 24px;
}

.keypad {
  display: grid;
  grid-template-columns: repeat(3, 80px);
  grid-gap: 10px;
}

.keypad button {
  width: 80px;
  height: 80px;
  font-size: 24px;
  cursor: pointer;
}

.login-button {
  background-color: orange;
  border: none;
  color: white;
}

.login-button:hover {
  background-color: darkorange;
}
