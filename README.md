    <div style={inputDisplayStyle}>
        {Array.from({ length: 4 }, (_, i) => (
          <div key={i} style={circleStyle}>
            {/* {input[i] || ""} */}
          </div>
        ))}
      </div>


///

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
