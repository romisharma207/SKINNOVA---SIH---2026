# System Architecture - SKINNOVA

## How App Works (Flow)

User -> Takes Photo -> AI Model -> Analysis -> Recommendation -> Doctor (if needed)

## Step-by-Step Flow
1.  User opens app and clicks photo of skin issue
2.  Photo goes to AI Model (TensorFlow Lite) on cloud
3.  AI detects: Acne / Eczema / Pigmentation / Normal
4.  If Normal/Mild: Show product recommendation + daily routine
5.  If Serious: Show "Consult Doctor" button + list of dermatologists
6.  User can track progress daily

## Architecture Diagram (Text)

[Mobile App - Flutter]
      |
[Firebase Auth & Storage]
      |
[Backend API - Python Flask]
      |
[AI Model - CNN Trained on HAM10000]
      |
[Database - Firebase Firestore]

## Modules
- Auth Module: Login/Signup
- Image Processing: Crop + Enhance photo
- AI Inference: Predict disease
- Recommendation Engine: Rule-based product suggestion
- Doctor Module: Video call API
- Tracker Module: Save progress

## Data Privacy
- All photos encrypted
- User can delete data anytime
- No data shared with 3rd party
