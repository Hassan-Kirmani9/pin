![bg-poslogin](https://github.com/Hassan-Kirmani9/pin/assets/152422845/184b91f6-f18b-47fd-92d1-fe6d728ef775)
import React, { useState } from "react";

const Keypad = () => {
  const [input, setInput] = useState("");

  const handleButtonClick = (value) => {
    if (input.length < 4) {
      setInput(input + value);
    }
  };

  const handleClear = () => {
    setInput("");
  };

  const handleLogin = () => {
    alert(`Login with PIN: ${input}`);
  };

  const containerStyle = {
    display: "flex",
    flexDirection: "column",
    alignItems: "center",
    justifyContent: "center",
    height: "100vh",
  };

  const inputDisplayStyle = {
    display: "flex",
    justifyContent: "center",
    marginBottom: "20px",
  };

  const circleStyle = {
    width: "40px",
    height: "40px",
    borderRadius: "50%",
    border: "2px solid black",
    margin: "0 5px",
    display: "flex",
    alignItems: "center",
    justifyContent: "center",
    fontSize: "24px",
  };

  const keypadStyle = {
    display: "grid",
    gridTemplateColumns: "repeat(3, 80px)",
    gridGap: "10px",
  };

  const buttonStyle = {
    width: "80px",
    height: "80px",
    fontSize: "24px",
    cursor: "pointer",
  };

  const loginButtonStyle = {
    ...buttonStyle,
    backgroundColor: "orange",
    border: "none",
    color: "white",
  };

  const loginButtonHoverStyle = {
    backgroundColor: "darkorange",
  };

  return (
    <div style={containerStyle}>
      <div style={inputDisplayStyle}>
        {Array.from({ length: 4 }, (_, i) => (
          <div key={i} style={circleStyle}>
            {input[i] ? "*" : ""}
          </div>
        ))}
      </div>
      <div style={keypadStyle}>
        {[1, 2, 3].map((num) => (
          <button
            key={num}
            style={buttonStyle}
            onClick={() => handleButtonClick(num.toString())}
          >
            {num}
          </button>
        ))}
        {[4, 5, 6].map((num) => (
          <button
            key={num}
            style={buttonStyle}
            onClick={() => handleButtonClick(num.toString())}
          >
            {num}
          </button>
        ))}
        {[7, 8, 9].map((num) => (
          <button
            key={num}
            style={buttonStyle}
            onClick={() => handleButtonClick(num.toString())}
          >
            {num}
          </button>
        ))}
        <button style={buttonStyle} onClick={handleClear}>
          CLEAR
        </button>
        <button style={buttonStyle} onClick={() => handleButtonClick("0")}>
          0
        </button>
        <button
          style={loginButtonStyle}
          onClick={handleLogin}
          onMouseOver={(e) =>
            (e.currentTarget.style.backgroundColor =
              loginButtonHoverStyle.backgroundColor)
          }
          onMouseOut={(e) =>
            (e.currentTarget.style.backgroundColor =
              loginButtonStyle.backgroundColor)
          }
        >
          LOGIN
        </button>
      </div>
    </div>
  );
};

export default Keypad;

![bg-poslogin](https://github.com/Hassan-Kirmani9/pin/assets/152422845/65998b79-60b4-4f83-bf0a-ef29f1c3f8f8)


background: rgb(255,0,0);
background: linear-gradient(246deg, rgba(255,0,0,0.5766028823638831) 0%, rgba(255,255,255,1) 43%, rgba(0,5,255,0.6634376162574405) 100%);

