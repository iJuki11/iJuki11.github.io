/* Category Section */
.categories {
    display: flex;
    justify-content: center;
    gap: 50px;
    font-size: 24px;
    margin-top: 50px;
    font-weight: bold;
    position: relative;
}

/* Category Base Style */
.category {
    position: relative;
    cursor: pointer;
    padding-bottom: 5px;
    display: inline-block;
    padding: 10px 20px; /* Add some padding for better hover effect */
    transition: background-color 0.3s, color 0.3s; /* Smooth transition for background and color */
}

/* When hovering on the category container */
.category:hover {
    background-color: white;
    color: black;
}

/* When hovering over the text itself */
.category:hover span {
    color: gold; /* Gold color on hover */
}

.category::after {
    content: "";
    display: block;
    width: 100%;
    height: 2px;
    background-color: white;
    margin-top: 5px;
    transition: all 0.3s ease;
}

.category:hover::after {
    width: 100%;
    height: 4px;
    background-color: rgba(75, 114, 180, 1);
    position: absolute;
    bottom: 0;
    left: 0;
}

/* Hover Animation for Shipped Projects */
.category:hover {
    font-size: 28px; /* Increase font size on hover */
    transform: scale(1.1);
    transition: all 0.3s ease;
}

/* For the text to change color */
.category span {
    transition: color 0.3s ease; /* Add smooth transition for text color */
}
