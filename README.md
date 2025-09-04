ai-interview-coach/
├── app/
│   ├── __init__.py              # Flask app setup (register blueprints, DB, etc.)
│   │
│   ├── routes/                  # Controllers (endpoints)
│   │   ├── __init__.py
│   │   ├── auth.py              # Login/Register
│   │   ├── resume.py            # Resume upload + parsing
│   │   ├── questions.py         # Generate role-based questions
│   │   ├── interview.py         # Mock interview handling
│   │   ├── analysis.py          # Analyze responses
│   │   └── feedback.py          # Generate final feedback
│   │
│   ├── services/                # Business logic (AI/NLP/ML parts)
│   │   ├── __init__.py
│   │   ├── nlp_resume_parser.py # NLP resume parsing
│   │   ├── role_mapping.py      # Match resume to role
│   │   ├── question_generator.py# AI-based Q generation
│   │   ├── body_language.py     # CV model for body language analysis
│   │   ├── grammar_check.py     # NLP grammar/language analysis
│   │   ├── skill_analysis.py    # Domain-specific skill check
│   │   └── scoring.py           # ATS score + Interview score
│   │
│   ├── models/                  # Database models (SQLAlchemy ORM)
│   │   ├── __init__.py
│   │   ├── user.py              # User model
│   │   ├── resume.py            # Resume model
│   │   ├── role.py              # Role model
│   │   ├── question.py          # Questions model
│   │   ├── interviews.py         # Interview sessions
│   │   ├── response.py          # User responses
│   │   └── feedback.py          # Feedback model
│   │
│   ├── templates/               # Frontend HTML (Jinja2 templates)
│   │   ├── base.html            # Common layout (header/footer)
│   │   ├── index.html           # Landing page
│   │   ├── login.html
│   │   ├── register.html
│   │   ├── home.html            # Resume upload + role selection
│   │   ├── questions.html
│   │   ├── mock_interview.html
│   │   └── feedback.html
│   │
│   ├── static/                  # CSS, JS, images
│   │   ├── css/
│   │   │   ├── style.css
│   │   │   ├── home.css
│   │   │   └── interview.css
│   │   ├── js/
│   │   │   ├── main.js
│   │   │   └── interview.js
│   │   └── img/
│   │       └── logo.png
│   │
│   └── utils/                   # Helper utilities
│       ├── __init__.py
│       ├── file_handler.py      # Resume upload/save
│       ├── video_audio_utils.py # For audio/video recordings
│       └── text_cleaner.py      # Cleaning text before NLP
│
├── migrations/                  # Alembic migrations (DB schema versions)
├── instance/
│   ├── uploads/                 # Uploaded resumes & recordings
│   └── config.py                # Local configuration
│
├── tests/                       # Unit & integration tests
│   ├── test_resume.py
│   ├── test_questions.py
│   ├── test_interview.py
│   └── test_feedback.py
│
├── venv/                        # Virtual environment (ignored in git)
├── run.py                       # Flask app entry point
├── requirements.txt             # Python dependencies
└── README.md
