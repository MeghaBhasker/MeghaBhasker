import React, { useState } from 'react';
import { PhoneCall, Linkedin, Mail, ExternalLink } from 'lucide-react';

const Portfolio = () => {
  const portfolioData = {
    name: "Megha Bhasker",
    title: "Associate Product Manager",
    tagline: "Building innovative products at the intersection of technology and user experience",
    about: "Associate Product Manager at EarthDefine managing the Buildings API product, delivering geospatial intelligence to enterprise clients. Proven track record in product strategy, market analysis, and cross-functional leadership through academic projects and internships at Venba Tech and Customer Analytics LLC. Passionate about creating data-driven products that solve real-world problems.",
    
    skills: {
      "Product Management": ["Product Strategy & Roadmapping", "Market Research & Analysis", "User Research & Testing", "Product Requirements (PRD)", "Go-to-Market Strategy"],
      "Technical": ["API Product Management", "Data Analytics & PowerBI", "Geospatial Technology", "Python & R", "Technical Documentation"],
      "Leadership": ["Cross-functional Team Leadership", "Stakeholder Management", "Risk Analysis & DFMEA", "Agile Methodologies"]
    },
    
    experience: [
      {
        title: "Buildings API Product Management",
        company: "EarthDefine",
        location: "Remote",
        period: "Current Role",
        description: "Associate Product Manager for geospatial intelligence platform serving building data across the United States.",
        bullets: [
          "●Managing end-to-end product roadmap for Buildings API, prioritizing features based on customer feedback and market analysis to support address-based, coordinate-based, and region-of-interest (ROI) query capabilities",
          "●Collaborating with engineering team to define technical specifications and API endpoints, ensuring 99.9% uptime and sub-200ms response times for enterprise clients",
          "●Driving product strategy and go-to-market initiatives, creating comprehensive technical documentation and integration guides to accelerate client onboarding by 35%",
          "●Conducting competitive analysis of geospatial data providers to identify product differentiation opportunities and feature gaps"
        ],
        technologies: ["API Product Management", "Geospatial Technology", "Product Roadmap", "Technical Documentation"]
      },
      {
        title: "Product Manager Intern - PowerBI Analytics",
        company: "Venba Tech",
        location: "Chennai, India",
        period: "May 2022 - Aug 2022",
        description: "Led data visualization initiative for enterprise clients, managing team of data engineer interns.",
        bullets: [
          "●Designed and deployed 3 comprehensive PowerBI dashboards for major clients including Reliance, Cafe Coffee Day, and Raintree Hotels, providing real-time product health insights to 20+ external stakeholders",
          "●Managed team of 3 data engineer interns through sprint planning and code reviews, improving team velocity by 40% and reducing dashboard load times by 50%",
          "●Architected holistic monitoring system tracking usage growth, store occupancy, and customer engagement metrics across 15+ KPIs, improving decision-making efficiency by 40%",
          "●Led web marketing strategy and social media roadmap for MysaIoT Products, increasing brand engagement by 35% and driving 25% growth in qualified lead generation over 3-month period"
        ],
        technologies: ["PowerBI", "Data Analytics", "Team Leadership", "Product Strategy", "KPI Development"]
      },
      {
        title: "Product Development Research Intern",
        company: "Customer Analytics LLC",
        location: "Chennai, India",
        period: "Dec 2021 - Apr 2022",
        description: "Developed IoT-based prototype solutions for industrial manufacturing efficiency.",
        bullets: [
          "●Improved CNC coolant efficiency by 30% through deployment of Arduino-based sensor system with M5StickC Plus, developing 6 functional prototypes with real-time monitoring capabilities",
          "●Conducted user research with 10+ manufacturing floor operators to identify pain points and validate product-market fit for IoT monitoring solution",
          "●Created technical specifications and product roadmap for scaling prototype to production-ready industrial IoT solution"
        ],
        technologies: ["IoT Product Development", "Arduino", "User Research", "Technical Prototyping"]
      }
    ],

    projects: [
      {
        title: "ProActiveSense - Fitness Wearable Product Strategy",
        type: "Academic Project",
        course: "Advanced Product Development, Northeastern University",
        period: "Dec 2023",
        mentor: "Professor John Deane (National Manager, Market Development - Boston Scientific)",
        description: "Led cross-functional team of 4 members developing comprehensive product strategy for innovative fitness wearable technology targeting competitive athletes and fitness enthusiasts.",
        bullets: [
          "●Conducted primary market research with 80+ fitness enthusiasts and competitive analysis across 5+ wearable brands (Apple Watch, Whoop, Garmin, Fitbit), identifying $3B total addressable market (TAM) in Massachusetts region with projected $120M first-year revenue at 50% gross margin",
          "●Engineered detailed product specifications for IMU sensor-based wearable with ML-powered exercise detection, defining 150+ trackable movements, automatic rep counting with 95% accuracy target, and real-time form correction feedback",
          "●Executed comprehensive Design Failure Mode and Effects Analysis (DFMEA) identifying 10+ critical failure modes including sensor calibration, battery life, and water resistance, implementing risk mitigation strategies reducing overall Risk Priority Number (RPN) by 65%",
          "●Developed business canvas model and stakeholder engagement matrix encompassing 9+ key partners (sensor suppliers, manufacturers, distribution channels, fitness instructors), defining clear communication and value proposition strategies",
          "●Created go-to-market strategy with tiered pricing model ($299.99 device + $9.99/month subscription) and distribution partnerships with 5,000+ gyms across Massachusetts, targeting 10% market penetration in year one"
        ],
        deliverables: [
          "Market Research Report & Competitive Analysis",
          "Product Requirements Document (PRD)",
          "DFMEA Risk Analysis Matrix",
          "Business Canvas Model",
          "Go-to-Market Strategy & Revenue Projections"
        ],
        technologies: ["Product Strategy", "Market Analysis", "DFMEA", "Technical Specifications", "Business Modeling"],
        impact: "Projected $120M revenue, 10% market penetration"
      },
      {
        title: "Robotics Project Management - Industrial Automation",
        type: "Academic Project",
        course: "Engineering Project Management, Northeastern University",
        period: "Apr 2023",
        mentor: "Professor George Kontopidis (Director of Systems and Software - Bose Corporation)",
        description: "Applied project management methodologies to industrial robotics implementation.",
        bullets: [
          "●Built and programmed 7 industrial robots for manufacturing automation scenarios, applying project management best practices including WBS (Work Breakdown Structure) and resource allocation",
          "●Designed comprehensive project charter defining scope, objectives, stakeholders, and success criteria for robotics deployment in simulated factory environment",
          "●Developed detailed project timeline using Gantt charts, managing dependencies across hardware assembly, software programming, and testing phases to deliver project 10% under timeline",
          "●Conducted risk assessment and mitigation planning for common robotics failures including sensor malfunction, calibration drift, and safety protocol violations"
        ],
        technologies: ["Project Management", "Gantt Charts", "Risk Management", "Industrial Robotics"],
        impact: "Delivered 7 robots 10% ahead of schedule"
      }
    ],

    education: [
      {
        degree: "Master of Science in Engineering Management",
        school: "Northeastern University",
        location: "Boston, MA",
        period: "Sep 2022 - May 2024",
        highlights: [
          "Relevant Coursework: Advanced Product Management, Product Development, Engineering Project Management",
          "Vice President - Marketing & Communications, Aspiring Product Managers Club (APMC)",
          "Organized Product Conference featuring industry leaders, connecting 200+ students with product professionals"
        ]
      },
      {
        degree: "Bachelor of Technology in Electronics and Communication Engineering",
        school: "Vellore Institute of Technology (VIT) Chennai",
        location: "Chennai, India",
        period: "Aug 2018 - Aug 2022",
        highlights: [
          "Head of Marketing & Sponsorship - Vsplash Tech Fest",
          "Secured sponsorships worth ₹375K for annual technical festival 'Vibrance'"
        ]
      }
    ],

    publications: [
      {
        title: "IoT-based Control System for Home Automation",
        type: "Research Paper",
        description: "Published technical paper on connected device architecture for smart home applications"
      },
      {
        title: "Smart Home Security System with Arduino & IoT",
        type: "Research Paper",
        description: "Research on implementing real-time security monitoring using IoT sensor networks"
      }
    ],

    extracurriculars: [
      {
        title: "VP of Marketing & Communications",
        organization: "Aspiring Product Managers Club (APMC), Northeastern University",
        period: "2023-2024",
        description: "Led marketing and communications strategy for 300+ member product management club",
        achievements: [
          "Organized flagship Product Conference featuring speakers from Amazon, Microsoft, and startups, attracting 200+ attendees",
          "Developed conference roadmap including speaker acquisition, event logistics, and promotional strategy",
          "Managed social media presence and email campaigns, growing club membership by 45% year-over-year",
          "Created marketing content and managed partnerships with 5+ corporate sponsors"
        ]
      },
      {
        title: "Head of Marketing & Sponsorship",
        organization: "Vsplash - VIT Chennai Tech Fest",
        period: "2020-2021",
        description: "Led sponsorship acquisition and marketing strategy for annual technical festival",
        achievements: [
          "Secured sponsorships worth ₹375,000 for 'Vibrance' tech fest through strategic corporate partnerships",
          "Managed marketing campaigns reaching 10,000+ students across South India universities",
          "Coordinated with 15+ corporate sponsors including tech companies and local businesses"
        ]
      },
      {
        title: "Cultural Secretary",
        organization: "Chettinad Vidyashram",
        period: "2015-2018",
        description: "Led cultural event planning and sponsor acquisition for city's largest high school cultural festival",
        achievements: [
          "Acquired sponsorships worth ₹150,000 for 'Maithri' - Chennai's biggest high school cultural fest",
          "Organized events attracting 2,000+ participants across 20+ schools in Chennai"
        ]
      }
    ],

    interests: [
      {
        title: "Bharatnatyam Dance",
        description: "Classical Indian dancer with 18+ years of training since age 5",
        icon: "💃"
      },
      {
        title: "Chess",
        description: "Competitive chess player and strategic thinking enthusiast",
        icon: "♟️"
      },
      {
        title: "Product Thinking",
        description: "Avid reader of product management blogs, case studies, and tech trends",
        icon: "💡"
      }
    ],

    contact: {
      email: "bhasker.me@northeastern.edu",
      phone: "857-225-9359",
      linkedin: "https://linkedin.com/in/meghabhask"
    },

    featuredLinks: [
      {
        title: "Product Conference Success - APMC",
        url: "https://www.linkedin.com/posts/meghabhasker_aspiringproductmanagersclub-productconferencesuccess-activity-7180795978633883648-Knnt",
        description: "Successfully organized and executed the APMC Product Conference at Northeastern University, featuring industry leaders and connecting students with product management professionals."
      }
    ]
  };

  return (
    <div className="min-h-screen bg-gradient-to-br from-pink-50 via-white to-purple-50">
      {/* Header */}
      <header className="bg-white shadow-lg">
        <div className="max-w-5xl mx-auto py-20 px-6 bg-gradient-to-r from-pink-100 via-purple-50 to-pink-100">
          <h1 className="text-5xl font-bold text-gray-800 mb-3">{portfolioData.name}</h1>
          <h2 className="text-2xl text-purple-700 font-semibold mb-3">{portfolioData.title}</h2>
          <p className="text-lg text-purple-600 mb-6 italic">{portfolioData.tagline}</p>
          <p className="text-base text-gray-700 max-w-3xl leading-relaxed">{portfolioData.about}</p>
          
          <div className="flex gap-6 mt-6 flex-wrap">
            <a href={`mailto:${portfolioData.contact.email}`} className="flex items-center gap-2 text-purple-600 hover:text-purple-800 transition-colors">
              <Mail className="w-5 h-5" />
              <span className="text-sm">{portfolioData.contact.email}</span>
            </a>
            <a href={`tel:${portfolioData.contact.phone}`} className="flex items-center gap-2 text-purple-600 hover:text-purple-800 transition-colors">
              <PhoneCall className="w-5 h-5" />
              <span className="text-sm">{portfolioData.contact.phone}</span>
            </a>
            <a href={portfolioData.contact.linkedin} target="_blank" rel="noopener noreferrer" className="flex items-center gap-2 text-purple-600 hover:text-purple-800 transition-colors">
              <Linkedin className="w-5 h-5" />
              <span className="text-sm">LinkedIn</span>
            </a>
          </div>
        </div>
      </header>

      <div className="max-w-5xl mx-auto px-6">
        {/* Professional Experience */}
        <section className="py-12">
          <h2 className="text-3xl font-bold text-gray-800 mb-8 border-b-2 border-purple-200 pb-2">Professional Experience</h2>
          <div className="space-y-8">
            {portfolioData.experience.map((exp, index) => (
              <div key={index} className="bg-white rounded-lg shadow-md p-6 hover:shadow-lg transition-all duration-300 border-l-4 border-purple-400">
                <div className="flex justify-between items-start mb-3">
                  <div>
                    <h3 className="text-xl font-bold text-gray-800">{exp.title}</h3>
                    <p className="text-purple-700 font-semibold">{exp.company} • {exp.location}</p>
                    <p className="text-gray-500 text-sm">{exp.period}</p>
                  </div>
                </div>
                <p className="text-gray-700 mb-4 italic">{exp.description}</p>
                <ul className="space-y-2 mb-4">
                  {exp.bullets.map((bullet, idx) => (
                    <li key={idx} className="text-gray-600 text-sm leading-relaxed pl-4 border-l-2 border-pink-200">
                      {bullet}
                    </li>
                  ))}
                </ul>
                <div className="flex flex-wrap gap-2">
                  {exp.technologies.map((tech, idx) => (
                    <span key={idx} className="bg-gradient-to-r from-pink-100 to-purple-100 text-purple-700 px-3 py-1 rounded-full text-xs font-medium">
                      {tech}
                    </span>
                  ))}
                </div>
              </div>
            ))}
          </div>
        </section>

        {/* Projects */}
        <section className="py-12">
          <h2 className="text-3xl font-bold text-gray-800 mb-8 border-b-2 border-purple-200 pb-2">Academic Projects</h2>
          <div className="space-y-6">
            {portfolioData.projects.map((project, index) => (
              <div key={index} className="bg-white rounded-lg shadow-md p-6 hover:shadow-lg transition-all duration-300 border border-pink-100">
                <div className="flex justify-between items-start mb-3">
                  <div className="flex-1">
                    <h3 className="text-xl font-bold text-gray-800">{project.title}</h3>
                    <p className="text-sm text-purple-600 font-semibold">{project.course}</p>
                    {project.mentor && <p className="text-xs text-gray-500 italic mt-1">Mentor: {project.mentor}</p>}
                    <p className="text-xs text-gray-500">{project.period}</p>
                  </div>
                  <span className="bg-pink-100 text-purple-700 px-3 py-1 rounded-full text-xs font-semibold">
                    {project.type}
                  </span>
                </div>
                
                <p className="text-gray-700 mb-4 font-medium">{project.description}</p>
                
                <ul className="space-y-2 mb-4">
                  {project.bullets.map((bullet, idx) => (
                    <li key={idx} className="text-gray-600 text-sm leading-relaxed pl-4 border-l-2 border-pink-200">
                      {bullet}
                    </li>
                  ))}
                </ul>

                {project.deliverables && (
                  <div className="mb-4">
                    <p className="text-sm font-semibold text-gray-700 mb-2">Key Deliverables:</p>
                    <div className="flex flex-wrap gap-2">
                      {project.deliverables.map((item, idx) => (
                        <span key={idx} className="bg-purple-50 text-purple-700 px-2 py-1 rounded text-xs">
                          {item}
                        </span>
                      ))}
                    </div>
                  </div>
                )}

                {project.impact && (
                  <p className="text-sm text-gray-700 mb-4">
                    <span className="font-semibold">Impact: </span>{project.impact}
                  </p>
                )}
                
                <div className="flex flex-wrap gap-2">
                  {project.technologies.map((tech, idx) => (
                    <span key={idx} className="bg-gradient-to-r from-pink-100 to-purple-100 text-purple-700 px-3 py-1 rounded-full text-xs font-medium">
                      {tech}
                    </span>
                  ))}
                </div>
              </div>
            ))}
          </div>
        </section>

        {/* Skills */}
        <section className="py-12">
          <h2 className="text-3xl font-bold text-gray-800 mb-8 border-b-2 border-purple-200 pb-2">Skills & Expertise</h2>
          <div className="grid md:grid-cols-3 gap-6">
            {Object.entries(portfolioData.skills).map(([category, skills], index) => (
              <div key={index} className="bg-white rounded-lg shadow-md p-6 border border-pink-100">
                <h3 className="text-lg font-bold text-purple-700 mb-4">{category}</h3>
                <ul className="space-y-2">
                  {skills.map((skill, idx) => (
                    <li key={idx} className="text-gray-700 text-sm flex items-start">
                      <span className="text-purple-500 mr-2">▸</span>
                      {skill}
                    </li>
                  ))}
                </ul>
              </div>
            ))}
          </div>
        </section>

        {/* Education */}
        <section className="py-12">
          <h2 className="text-3xl font-bold text-gray-800 mb-8 border-b-2 border-purple-200 pb-2">Education</h2>
          <div className="space-y-6">
            {portfolioData.education.map((edu, index) => (
              <div key={index} className="bg-white rounded-lg shadow-md p-6 border-l-4 border-purple-400">
                <div className="flex justify-between items-start mb-3">
                  <div>
                    <h3 className="text-xl font-bold text-gray-800">{edu.degree}</h3>
                    <p className="text-purple-700 font-semibold">{edu.school}</p>
                    <p className="text-gray-500 text-sm">{edu.location} • {edu.period}</p>
                  </div>
                </div>
                {edu.highlights && (
                  <ul className="space-y-1 mt-3">
                    {edu.highlights.map((highlight, idx) => (
                      <li key={idx} className="text-gray-600 text-sm flex items-start">
                        <span className="text-purple-500 mr-2">•</span>
                        {highlight}
                      </li>
                    ))}
                  </ul>
                )}
              </div>
            ))}
          </div>
        </section>

        {/* Publications */}
        <section className="py-12">
          <h2 className="text-3xl font-bold text-gray-800 mb-8 border-b-2 border-purple-200 pb-2">Publications</h2>
          <div className="grid md:grid-cols-2 gap-6">
            {portfolioData.publications.map((pub, index) => (
              <div key={index} className="bg-white rounded-lg shadow-md p-6 border border-pink-100">
                <h3 className="text-lg font-semibold text-gray-800 mb-2">{pub.title}</h3>
                <p className="text-sm text-purple-600 mb-2">{pub.type}</p>
                <p className="text-sm text-gray-600">{pub.description}</p>
              </div>
            ))}
          </div>
        </section>

        {/* Leadership & Extracurriculars */}
        <section className="py-12">
          <h2 className="text-3xl font-bold text-gray-800 mb-8 border-b-2 border-purple-200 pb-2">Leadership & Extracurriculars</h2>
          <div className="space-y-6">
            {portfolioData.extracurriculars.map((activity, index) => (
              <div key={index} className="bg-white rounded-lg shadow-md p-6 border border-pink-100">
                <div className="flex justify-between items-start mb-3">
                  <div>
                    <h3 className="text-lg font-bold text-gray-800">{activity.title}</h3>
                    <p className="text-purple-600 font-semibold text-sm">{activity.organization}</p>
                    <p className="text-gray-500 text-xs">{activity.period}</p>
                  </div>
                </div>
                <p className="text-gray-700 text-sm mb-3 italic">{activity.description}</p>
                <ul className="space-y-1">
                  {activity.achievements.map((achievement, idx) => (
                    <li key={idx} className="text-gray-600 text-sm flex items-start">
                      <span className="text-purple-500 mr-2">•</span>
                      {achievement}
                    </li>
                  ))}
                </ul>
              </div>
            ))}
          </div>
        </section>

        {/* Personal Interests */}
        <section className="py-12">
          <h2 className="text-3xl font-bold text-gray-800 mb-8 border-b-2 border-purple-200 pb-2">Personal Interests</h2>
          <div className="grid md:grid-cols-3 gap-6">
            {portfolioData.interests.map((interest, index) => (
              <div key={index} className="bg-white rounded-lg shadow-md p-6 text-center border border-pink-100 hover:shadow-lg transition-all">
                <div className="text-4xl mb-3">{interest.icon}</div>
                <h3 className="text-lg font-bold text-gray-800 mb-2">{interest.title}</h3>
                <p className="text-sm text-gray-600">{interest.description}</p>
              </div>
            ))}
          </div>
        </section>

        {/* Featured Content */}
        {portfolioData.featuredLinks.length > 0 && (
          <section className="py-12">
            <h2 className="text-3xl font-bold text-gray-800 mb-8 border-b-2 border-purple-200 pb-2">Featured</h2>
            <div className="grid md:grid-cols-1 gap-6">
              {portfolioData.featuredLinks.map((link, index) => (
                
                  key={index}
                  href={link.url}
                  target="_blank"
                  rel="noopener noreferrer"
                  className="bg-gradient-to-r from-pink-50 to-purple-50 rounded-lg shadow-md p-6 hover:shadow-lg transition-all duration-300 border border-purple-200 group"
                >
                  <div className="flex justify-between items-start">
                    <div>
                      <h3 className="text-xl font-bold text-gray-800 mb-2 group-hover:text-purple-700 transition-colors">{link.title}</h3>
                      <p className="text-gray-600 mb-4">{link.description}</p>
                      <div className="flex items-center text-purple-600 group-hover:text-purple-800">
                        <span className="font-semibold">View on LinkedIn</span>
                        <ExternalLink className="w-4 h-4 ml-2" />
                      </div>
                    </div>
                  </div>
                </a>
              ))}
            </div>
          </section>
        )}
      </div>

      {/* Footer */}
      <footer className="bg-gradient-to-r from-pink-100 via-purple-50 to-pink-100 mt-16 py-12">
        <div className="max-w-5xl mx-auto px-6 text-center">
          <h2 className="text-2xl font-bold text-gray-800 mb-6">Let's Connect</h2>
          <p className="text-gray-700 mb-6">I'm always interested in discussing product management, innovative projects, and collaboration opportunities.</p>
          <div className="flex gap-6 justify-center flex-wrap">
            <a href={`mailto:${portfolioData.contact.email}`} className="flex items-center gap-2 text-purple-600 hover:text-purple-800 transition-colors font-semibold">
              <Mail className="w-5 h-5" />
              <span>Email Me</span>
            </a>
            <a href={portfolioData.contact.linkedin} target="_blank" rel="noopener noreferrer" className="flex items-center gap-2 text-purple-600 hover:text-purple-800 transition-colors font-semibold">
              <Linkedin className="w-5 h-5" />
              <span>Connect on LinkedIn</span>
            </a>
          </div>
        </div>
      </footer>
    </div>
  );
};

export default Portfolio;
