const containerStyle = {
    display: "flex",
    flexDirection: "column",
    alignItems: "center",
    justifyContent: "center",
    height: "100vh",
  };

  const inputStyle = {
    width: "200px",
    height: "40px",
    textAlign: "center",
    marginBottom: "20px",
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

///////
    <div style={containerStyle}>
      <input type="password" readOnly style={inputStyle} />
      <div style={keypadStyle}>
        {[1, 2, 3].map((num) => (
          <button key={num} style={buttonStyle}>
            {num}
          </button>
        ))}
        {[4, 5, 6].map((num) => (
          <button key={num} style={buttonStyle}>
            {num}
          </button>
        ))}
        {[7, 8, 9].map((num) => (
          <button key={num} style={buttonStyle}>
            {num}
          </button>
        ))}
        <button style={buttonStyle}>CLEAR</button>
        <button style={buttonStyle}>0</button>
        <button
          style={loginButtonStyle}
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
