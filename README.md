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
