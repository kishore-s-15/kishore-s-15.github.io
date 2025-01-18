---
layout: page
title: personal
permalink: /personal/
description: Explore the world through my lens — a glimpse into the moments and perspectives that shape my journey.
nav: true
nav_order: 7
---

<style>
.photo-grid {
    display: grid;
    grid-template-columns: repeat(auto-fill, minmax(200px, 1fr));
    gap: 20px;
    padding: 20px 0;
}

.photo-item {
    width: 100%;
    cursor: pointer;
    transition: transform 0.3s ease;
}

.photo-item:hover {
    transform: scale(1.02);
}

.photo-container {
    position: relative;
    width: 100%;
    padding-bottom: 75%; /* 4:3 Aspect Ratio */
    overflow: hidden;
}

.photo-container img {
    position: absolute;
    width: 100%;
    height: 100%;
    object-fit: cover;
    border-radius: 8px;
}

.photo-caption {
    margin-top: 8px;
    font-size: 0.9em;
    color: var(--global-text-color-light);
    text-align: center;
    font-style: italic;
}

/* Modal styles */
.modal {
    display: none;
    position: fixed;
    z-index: 9999;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    background-color: rgba(0, 0, 0, 0.9);
    padding: 20px;
    justify-content: center;
    align-items: center;
}

.modal-content {
    max-width: 70%;
    max-height: 80vh;
    margin: auto;
    display: block;
    object-fit: contain;
}

.modal-close {
    position: fixed;
    top: 15px;
    right: 35px;
    color: #f1f1f1;
    font-size: 40px;
    font-weight: bold;
    cursor: pointer;
    z-index: 1001;
    padding: 10px;
}

.modal-close:hover {
    color: #fff;
}
</style>

### The world through my eyes

*Every photograph tells a unique story of discovery, wonder, and connection.*

#### New York City, USA 🗽

<div class="photo-grid">
    <div class="photo-item">
        <div class="photo-container">
            <img src="../assets/img/nyc/nyc_over_sea.jpg" alt="Times Square at night">
        </div>
        <div class="photo-caption">Flying over the seas of NYC</div>
    </div>
    
    <div class="photo-item">
        <div class="photo-container">
            <img src="../assets/img/nyc/nyc_over_suburbs.jpg" alt="Central Park in autumn">
        </div>
        <div class="photo-caption">The Suburbs of NYC seen through an Airbus</div>
    </div>
</div>

#### Musuem of Fine Arts, Boston 🏛️

<div class="photo-grid">
    <div class="photo-item">
        <div class="photo-container">
            <img src="../assets/img/mfa/mfa_1.jpg" alt="Golden Gate Bridge">
        </div>
        <div class="photo-caption">An iconic symbol of engineering and beauty, shrouded in morning fog</div>
    </div>
    
    <!-- <div class="photo-item">
        <div class="photo-container">
            <img src="../assets/img/mfa/mfa_2.jpg" alt="Golden Gate Bridge">
        </div>
        <div class="photo-caption">An iconic symbol of engineering and beauty, shrouded in morning fog</div>
    </div>
    
    <div class="photo-item">
        <div class="photo-container">
            <img src="../assets/img/mfa/mfa_3.jpg" alt="Golden Gate Bridge">
        </div>
        <div class="photo-caption">An iconic symbol of engineering and beauty, shrouded in morning fog</div>
    </div>

    <div class="photo-item">
        <div class="photo-container">
            <img src="../assets/img/mfa/mfa_4.jpg" alt="Golden Gate Bridge">
        </div>
        <div class="photo-caption">An iconic symbol of engineering and beauty, shrouded in morning fog</div>
    </div> -->

    <div class="photo-item">
        <div class="photo-container">
            <img src="../assets/img/mfa/mfa_5.JPG" alt="Golden Gate Bridge">
        </div>
        <div class="photo-caption">An iconic symbol of engineering and beauty, shrouded in morning fog</div>
    </div>
<!-- 
    <div class="photo-item">
        <div class="photo-container">
            <img src="../assets/img/mfa/mfa_6.jpg" alt="Golden Gate Bridge">
        </div>
        <div class="photo-caption">An iconic symbol of engineering and beauty, shrouded in morning fog</div>
    </div> -->

    <!-- <div class="photo-item">
        <div class="photo-container">
            <img src="../assets/img/mfa/mfa_7.jpg" alt="Golden Gate Bridge">
        </div>
        <div class="photo-caption">An iconic symbol of engineering and beauty, shrouded in morning fog</div>
    </div> -->

    <div class="photo-item">
        <div class="photo-container">
            <img src="../assets/img/mfa/mfa_8.JPG" alt="Golden Gate Bridge">
        </div>
        <div class="photo-caption">An iconic symbol of engineering and beauty, shrouded in morning fog</div>
    </div>
</div>

#### Boston, USA 🌃

<div class="photo-grid">
    <div class="photo-item">
        <div class="photo-container">
            <img src="../assets/img/boston/boston_1.jpg" alt="Golden Gate Bridge">
        </div>
        <div class="photo-caption">An iconic symbol of engineering and beauty, shrouded in morning fog</div>
    </div>
    
    <div class="photo-item">
        <div class="photo-container">
            <img src="../assets/img/boston/boston_2.jpg" alt="Golden Gate Bridge">
        </div>
        <div class="photo-caption">An iconic symbol of engineering and beauty, shrouded in morning fog</div>
    </div>
    
    <div class="photo-item">
        <div class="photo-container">
            <img src="../assets/img/boston/boston_3.jpg" alt="Golden Gate Bridge">
        </div>
        <div class="photo-caption">An iconic symbol of engineering and beauty, shrouded in morning fog</div>
    </div>

    <div class="photo-item">
        <div class="photo-container">
            <img src="../assets/img/boston/boston_4.jpg" alt="Golden Gate Bridge">
        </div>
        <div class="photo-caption">An iconic symbol of engineering and beauty, shrouded in morning fog</div>
    </div>

    <div class="photo-item">
        <div class="photo-container">
            <img src="../assets/img/boston/boston_5.jpg" alt="Golden Gate Bridge">
        </div>
        <div class="photo-caption">An iconic symbol of engineering and beauty, shrouded in morning fog</div>
    </div>

    <div class="photo-item">
        <div class="photo-container">
            <img src="../assets/img/boston/boston_6.jpg" alt="Golden Gate Bridge">
        </div>
        <div class="photo-caption">An iconic symbol of engineering and beauty, shrouded in morning fog</div>
    </div>

    <div class="photo-item">
        <div class="photo-container">
            <img src="../assets/img/boston/boston_7.jpg" alt="Golden Gate Bridge">
        </div>
        <div class="photo-caption">An iconic symbol of engineering and beauty, shrouded in morning fog</div>
    </div>

    <div class="photo-item">
        <div class="photo-container">
            <img src="../assets/img/boston/boston_8.jpg" alt="Golden Gate Bridge">
        </div>
        <div class="photo-caption">An iconic symbol of engineering and beauty, shrouded in morning fog</div>
    </div>

    <div class="photo-item">
        <div class="photo-container">
            <img src="../assets/img/boston/snowy_day.jpg" alt="Golden Gate Bridge">
        </div>
        <div class="photo-caption">An iconic symbol of engineering and beauty, shrouded in morning fog</div>
    </div>
</div>

#### Indian Institute of Technology, Madras 🎓

<div class="photo-grid">
    <div class="photo-item">
        <div class="photo-container">
            <img src="../assets/img/iitm_research_park/iitm_rp_1.jpg" alt="Golden Gate Bridge">
        </div>
        <div class="photo-caption">An iconic symbol of engineering and beauty, shrouded in morning fog</div>
    </div>
    
    <div class="photo-item">
        <div class="photo-container">
            <img src="../assets/img/iitm_research_park/iitm_rp_3.jpg" alt="Golden Gate Bridge">
        </div>
        <div class="photo-caption">An iconic symbol of engineering and beauty, shrouded in morning fog</div>
    </div>

    <div class="photo-item">
        <div class="photo-container">
            <img src="../assets/img/iitm_research_park/iitm.jpg" alt="Golden Gate Bridge">
        </div>
        <div class="photo-caption">An iconic symbol of engineering and beauty, shrouded in morning fog</div>
    </div>
</div>

#### Northeastern University 🎓

<div class="photo-grid">
    <div class="photo-item">
        <div class="photo-container">
            <img src="../assets/img/northeastern_university/neu_1.jpg" alt="Golden Gate Bridge">
        </div>
        <div class="photo-caption">An iconic symbol of engineering and beauty, shrouded in morning fog</div>
    </div>
    
    <div class="photo-item">
        <div class="photo-container">
            <img src="../assets/img/northeastern_university/neu_2.jpg" alt="Golden Gate Bridge">
        </div>
        <div class="photo-caption">An iconic symbol of engineering and beauty, shrouded in morning fog</div>
    </div>
</div>

#### Incredible India 🇮🇳

<div class="photo-grid">
    <div class="photo-item">
        <div class="photo-container">
            <img src="../assets/img/india/marina_chennai.jpg" alt="Golden Gate Bridge">
        </div>
        <div class="photo-caption">An iconic symbol of engineering and beauty, shrouded in morning fog</div>
    </div>
    
    <div class="photo-item">
        <div class="photo-container">
            <img src="../assets/img/india/trivandrum_kerala.jpg" alt="Golden Gate Bridge">
        </div>
        <div class="photo-caption">An iconic symbol of engineering and beauty, shrouded in morning fog</div>
    </div>
</div>

<!-- Modal -->
<div id="imageModal" class="modal">
    <span class="modal-close" id="modalClose">&times;</span>
    <img class="modal-content" id="modalImage">
</div>

<!-- JavaScript for modal functionality -->
<script>
// Get DOM elements
const modal = document.getElementById('imageModal');
const modalImage = document.getElementById('modalImage');
const closeButton = document.getElementById('modalClose');
const photoItems = document.querySelectorAll('.photo-item');

// Function to open modal
function openModal(imgElement) {
    modal.style.display = 'flex';
    modalImage.src = imgElement.src;
}

// Function to close modal
function closeModal() {
    modal.style.display = 'none';
}

// Add click event listeners to all photo items
photoItems.forEach(item => {
    const img = item.querySelector('img');
    item.addEventListener('click', () => openModal(img));
});

// Close modal when clicking the close button
closeButton.addEventListener('click', closeModal);

// Close modal when clicking outside the image
modal.addEventListener('click', (e) => {
    if (e.target === modal) {
        closeModal();
    }
});

// Close modal with escape key
document.addEventListener('keydown', (e) => {
    if (e.key === 'Escape') {
        closeModal();
    }
});
</script>