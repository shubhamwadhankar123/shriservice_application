// JavaScript to dynamically load service details
function showServiceDetails(serviceType) {
    const serviceImage = document.getElementById('service-image');
    const serviceDescription = document.getElementById('service-description');
    const serviceDetailsSection = document.getElementById('service-details');

    // Define details for each service type
    const serviceData = {
        healthWellnessFamily: {
            image: 'healthWellnessFamily.jpg',
            description: 'Comprehensive health and wellness services for families, including fitness plans, nutritional advice, and wellness workshops.'
        },
        educationChildcare: {
            image: 'educationChildcare.jpg',
            description: 'Educational support and childcare services to help families balance work and family life effectively.'
        },
        homeMaintenance: {
            image: 'homeMaintenance.jpg',
            description: 'Home maintenance services to keep your home in top shape, including plumbing, electrical, and general repairs.'
        },
        financialLegal: {
            image: 'financialLegal.jpg',
            description: 'Financial planning and legal advice services tailored for individuals and families.'
        },
        leisureEntertainment: {
            image: 'leisureEntertainment.jpg',
            description: 'Leisure and entertainment services to help families enjoy their free time and create lasting memories.'
        },
        transportationErrands: {
            image: 'transportationErrands.jpg',
            description: 'Transportation services and errand running to ease your daily commute and chores.'
        },
        healthWellnessSingle: {
            image: 'healthWellnessSingle.jpg',
            description: 'Health and wellness services tailored for individuals, focusing on fitness and personal well-being.'
        },
        homePersonalCare: {
            image: 'homePersonalCare.jpg',
            description: 'Home and personal care services to assist with daily activities and ensure comfort at home.'
        },
        socialDating: {
            image: 'socialDating.jpg',
            description: 'Social and dating services to help individuals connect and build relationships.'
        },
        financialCareer: {
            image: 'financialCareer.jpg',
            description: 'Career and financial coaching services to support personal and professional growth.'
        },
        leisureTravel: {
            image: 'leisureTravel.jpg',
            description: 'Travel planning and leisure services for unforgettable vacations and experiences.'
        },
        personalAssistance: {
            image: 'personalAssistance.jpg',
            description: 'Personal assistance services for busy professionals and families.'
        },
        elderlySpecialNeeds: {
            image: 'elderlySpecialNeeds.jpg',
            description: 'Specialized services for the elderly or those with special needs, ensuring care and support.'
        }
    };

    let serviceContent = '';

    switch (serviceType) {
        case 'healthWellnessFamily':
            serviceContent = `
                <h2>Health and Wellness Services (Family)</h2>
                <ul>
                    <li>Family health check-ups</li>
                    <li>Vaccination and immunization</li>
                    <li>Mental health counseling</li>
                    <li>Fitness and wellness programs</li>
                    <li>Nutritional guidance</li>
                </ul>`;
            break;
        case 'educationChildcare':
            serviceContent = `
                <h2>Education and Childcare</h2>
                <ul>
                    <li>Daycare services</li>
                    <li>After-school programs</li>
                    <li>Tutoring and academic support</li>
                    <li>Online learning platforms for kids</li>
                    <li>Parenting workshops</li>
                </ul>`;
            break;
        case 'homeMaintenance':
            serviceContent = `
                <h2>Home Maintenance</h2>
                <ul>
                    <li>House cleaning</li>
                    <li>Plumbing, electrical, and repair services</li>
                    <li>Gardening and landscaping</li>
                    <li>Pest control</li>
                    <li>HVAC (heating, ventilation, air conditioning) services</li>
                </ul>`;
            break;
        case 'financialLegal':
            serviceContent = `
                <h2>Financial and Legal Services</h2>
                <ul>
                    <li>Financial planning and budgeting</li>
                    <li>Tax preparation and filing</li>
                    <li>Estate planning and will services</li>
                    <li>Family legal services (e.g., divorce, child custody)</li>
                </ul>`;
            break;
        case 'leisureEntertainment':
            serviceContent = `
                <h2>Leisure and Entertainment</h2>
                <ul>
                    <li>Family vacation planning</li>
                    <li>Home entertainment installation</li>
                    <li>Event and party planning</li>
                </ul>`;
            break;
        case 'transportationErrands':
            serviceContent = `
                <h2>Transportation and Errands</h2>
                <ul>
                    <li>Family carpool services</li>
                    <li>Grocery delivery</li>
                    <li>Senior citizen transportation assistance</li>
                    <li>Personal shopping services</li>
                </ul>`;
            break;
        case 'healthWellnessSingle':
            serviceContent = `
                <h2>Health and Wellness Services (Single)</h2>
                <ul>
                    <li>Solo fitness training</li>
                    <li>Personal nutrition planning</li>
                    <li>Mental health and therapy sessions</li>
                    <li>Yoga and mindfulness programs</li>
                </ul>`;
            break;
        case 'homePersonalCare':
            serviceContent = `
                <h2>Home and Personal Care</h2>
                <ul>
                    <li>Housekeeping services</li>
                    <li>Laundry and dry-cleaning services</li>
                    <li>Home security and smart home setup</li>
                    <li>Grocery delivery services</li>
                </ul>`;
            break;
        case 'socialDating':
            serviceContent = `
                <h2>Social and Dating</h2>
                <ul>
                    <li>Online dating platforms</li>
                    <li>Social event organizing</li>
                    <li>Life coaching and self-development courses</li>
                </ul>`;
            break;
        case 'financialCareer':
            serviceContent = `
                <h2>Financial and Career Services</h2>
                <ul>
                    <li>Career coaching</li>
                    <li>Freelance job platforms</li>
                    <li>Retirement and investment planning</li>
                    <li>Tax and legal consultation</li>
                </ul>`;
            break;
        case 'leisureTravel':
            serviceContent = `
                <h2>Leisure and Travel</h2>
                <ul>
                    <li>Solo travel packages</li>
                    <li>Hobby classes and clubs (art, cooking, music)</li>
                    <li>Movie, concert, and event ticket booking</li>
                </ul>`;
            break;
        case 'personalAssistance':
            serviceContent = `
                <h2>Personal Assistance</h2>
                <ul>
                    <li>Personal shopping assistant</li>
                    <li>Virtual assistant services</li>
                    <li>Time management and productivity coaching</li>
                </ul>`;
            break;
        case 'elderlySpecialNeeds':
            serviceContent = `
                <h2>Services for Elderly or Special Needs</h2>
                <ul>
                    <li>In-home nursing care</li>
                    <li>Prescription delivery</li>
                    <li>Physiotherapy services</li>
                    <li>Medical equipment rental</li>
                </ul>`;
            break;
        default:
            serviceContent = `<h2>Select a service to see details</h2>`;
    }

    // Update the service details section
    if (serviceData[serviceType]) {
        serviceImage.src = serviceData[serviceType].image;
        serviceImage.alt = serviceType.replace(/([A-Z])/g, ' $1').trim(); // Format the alt text
        serviceDescription.innerHTML = serviceContent;

        // Show the image and description
        serviceImage.style.display = 'block';
        serviceDescription.style.display = 'block';
    } else {
        serviceImage.style.display = 'none';
        serviceDescription.style.display = 'none';
    }
}

// Additional functionality to handle login and signup
document.getElementById('loginForm')?.addEventListener('submit', function(event) {
    event.preventDefault();
    // Handle login logic here
    alert('Login functionality is not yet implemented.');
});

document.getElementById('signupForm')?.addEventListener('submit', function(event) {
    event.preventDefault();
    // Handle signup logic here
    alert('Signup functionality is not yet implemented.');
});
