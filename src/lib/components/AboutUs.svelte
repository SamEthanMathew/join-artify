<!-- Import necessary assets -->
<script>
    import greenWaves from '$lib/assets/greenWaves.svg';
    import path from '$lib/assets/path.png';
</script>

<!-- Main section for "About Us" -->
<section id="about-us">
    <!-- Decorative path image -->
    <img src={path} alt="" class="path" />
    
    <!-- Container for the about us text -->
    <div class="about-us-text-container">
        <h2>About Artify</h2>
        <p>
            Artify4Kids is a <span>non-profit</span> organization that aims to provide accessible
            <span>arts and crafts</span>
            education to underserved <span>children</span> in the <span>Bay Area</span>. Our mission is to
            foster <span>creativity, self-expression,</span> and <span>personal development</span>, while
            celebrating cultural diversity and promoting inclusivity in our art programs. Join us in
            empowering <span>young artists!</span>
        </p>
        <hr />
    </div>
    
    <!-- Container for the map and location info -->
    <div class="text-container">
        <iframe
            title="Bay Area Map"
            src="https://snazzymaps.com/embed/577090"
            width="100%"
            height="600px"
            style="border:none;"
            class="photo"
        ></iframe>
        <div class="text">
            <h2>Where?</h2>
            <p>Artify is based in the <span>Bay Area.</span></p>
        </div>
    </div>
    
    <!-- Container for the "How We Work" section -->
    <div class="text-container" id="right">
        <img src="/photos/how-we-work.webp" alt="" class="photo" id="hidden" />
        <div class="text">
            <h2>How We Work</h2>
            <p>
                We have weekly meetings to discuss current and future plans. Join us as we plan and carry
                out each <span>fundraiser</span>, <span>community events</span>, and
                <span>volunteer opportunities</span>.
            </p>
        </div>
        <img src="/photos/how-we-work.webp" alt="" class="photo" />
    </div>
    
    <!-- Clear floats -->
    <div class="clear"></div>
    
    <!-- Container for the learn more button -->
    <div class="btn-container">
        <a
            href="https://artify4kids.wixsite.com/website/about"
            target="_blank"
            rel="noopener noreferrer"
            id="apply"
        >
            <button class="btn">Learn More</button>
        </a>
    </div>
</section>

<!-- Decorative wave image -->
<img src={greenWaves} alt="" class="wave" />

<style>
    /* Hide element by default */
    #hidden {
        display: none;
    }

    /* Style for the buttons */
    button {
        width: 160px;
        z-index: 99;
    }

    /* Container for the button */
    .btn-container {
        display: flex;
        justify-content: center;
        margin-top: 40px;
        z-index: 999;
    }

    /* Style for the links */
    a {
        color: var(--violet);
    }

    /* Container for the about us text */
    .about-us-text-container {
        text-align: center;
        width: 70%;
        margin-left: auto;
        margin-right: auto;
        margin-bottom: 200px;
    }

    /* Container for general text sections */
    .text-container {
        display: flex;
        align-items: center;
        width: 70%;
        margin-top: 100px;
        margin-bottom: 90px;
    }

    /* Style for text within containers */
    .text {
        width: 60%;
        overflow-wrap: break-word;
    }

    /* Style for images within containers */
    .photo {
        width: 40%;
        border-radius: 18px;
        margin-left: 40px;
        margin-right: 40px;
        transition: 0.5s;
    }

    /* Hover effect for photos */
    .photo:hover {
        transform: scale(105%);
    }

    /* Style for iframe elements */
    iframe {
        height: 200px;
    }

    /* Align text to the right and float container right */
    #right {
        text-align: right;
        float: right;
    }

    /* Prevent user selection for images */
    img {
        user-select: none;
    }

    /* Style for emphasized text */
    span {
        color: var(--violet);
    }

    /* Style for paragraphs */
    p {
        line-height: 1.5rem;
        margin-bottom: 20px;
    }

    /* Center horizontal rule */
    hr {
        margin: auto;
    }

    /* Style for the path image */
    .path {
        margin-top: 110px;
        height: 900px;
        position: absolute;
        top: 50%;
        -ms-transform: translateY(-50%);
        transform: translateY(-50%);
        left: 50%;
        transform: translate(-50%, -50%);
        overflow: hidden;
        z-index: 0;
    }

    /* Clear both floats */
    .clear {
        clear: both;
    }

    /* Main container style for the about-us section */
    #about-us {
        height: 1200px;
        background-color: var(--green);
        padding-left: 20%;
        padding-right: 20%;
        padding-top: 60px;
        position: relative;
        color: var(--grey);
    }

    /* Style for the wave image */
    .wave {
        width: 100%;
        height: 60px;
        background-color: var(--blue);
    }

    /* Responsive styles for different screen sizes */
    @media (max-width: 1280px) {
        #about-us {
            padding-left: 10%;
            padding-right: 10%;
        }
        .about-us-text-container {
            width: 80%;
        }
        .text-container {
            width: 80%;
        }
    }

    @media (max-width: 1024px) {
        #about-us {
            padding-left: 5%;
            padding-right: 5%;
        }
        .about-us-text-container {
            width: 100%;
        }
    }

    @media (max-width: 768px) {
        .text-container {
            width: 90%;
        }
        .text-container {
            margin-bottom: 85px;
            margin-top: 85px;
        }
        h2 {
            font-size: 1.8rem;
        }
    }

    @media (max-width: 640px) {
        .path {
            display: none;
        }
        .text-container {
            width: 100%;
            flex-direction: column;
            margin-top: 10px;
            margin-bottom: 10px;
            text-align: center;
        }
        #right {
            text-align: center;
        }
        .about-us-text-container {
            margin-bottom: 60px;
        }
        #hidden {
            display: inline;
        }
        .photo {
            display: none;
        }
        .photo,
        iframe {
            width: 80%;
            margin-bottom: 20px;
        }
        .text {
            width: 100%;
        }
        #about-us {
            height: 1100px;
        }
    }
</style>