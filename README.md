# RES-VA Call Audit Tool

My very first app. A simple Streamlit dashboard that analyzes CSV call logs to flag problem calls and check campaign reachability.

## 🚀 Features

### **Security**
- Secure login for team members
- Pre-made user accounts
- Browser session memory

### **Call Flagging**
- Flags bad calls based on how long they lasted
- **Rules we use:**
  - Voicemails over 15 seconds
  - Dead calls over 15 seconds  
  - Decision Maker calls under 10 seconds
  - Wrong Numbers under 10 seconds
  - Unknown calls under 5 seconds

### **Filters**
- Filter the dashboard by agent
- Filter by campaign
- Both filters work independently of each other

### **Analytics & Dashboards**
- **Top Metrics**: Quick cards showing total flagged calls
- **Agent Stats**: Shows who is getting the most issues
- **Campaign Stats**: See how each campaign is performing
- **Flagged Calls Table**: A full list of every bad call
- **Charts**: Pie charts breaking down the statuses

### **Reachability Testing**
- Groups calls to see if campaigns are actually hitting leads
- **Low Engagement**: Dead Calls + Unknown + Voicemail
- **Good Engagement**: Decision Maker + Wrong Number
- Shows red/blue indicators so you know right away if a campaign is healthy

### **Exports**
- Download any filtered table directly to CSV
- Fixes bad CSV formatting automatically

## 📊 Dashboard Sections

### **1. Overall Summary**
- Metric cards showing total flagged calls
- Quick overview of campaign health
- Visual indicators for different issue types

### **2. Agent Summary**
- Performance breakdown by agent
- Total dead calls and unknown calls per agent
- Issue distribution across team members

### **3. Campaign Summary** *(Collapsible)*
- Campaign-specific disposition pie chart
- Reachability analysis with detailed reports
- Performance insights and recommendations

### **4. Flagged Calls**
- Detailed table of problematic calls
- Interactive disposition pie chart
- Summary cards with call type breakdowns

### **5. Export Data**
- Download functionality for filtered results
- CSV export with all relevant data

## 🛠️ Installation

### **Prerequisites**
- Python 3.7 or higher
- pip package manager

### **Setup Steps**
1. **Clone the repository**:
   ```bash
   git clone <repository-url>
   cd audit-detector
   ```

2. **Install dependencies**:
   ```bash
   pip install -r requirements.txt
   ```

3. **Run the application**:
   ```bash
   streamlit run audit2_app.py
   ```

4. **Access the app**:
   - Open your browser to `http://localhost:8501`
   - Login with authorized credentials

## 📁 File Structure

```
audit-detector/
├── audit2_app.py          # Main Streamlit application
├── main.py               # Recording download script
├── requirements.txt      # Python dependencies
├── call_log.csv         # Sample data file
├── vos_logo.png         # Application logo
└── README.md            # This file
```

## 🔧 Configuration

### **CSV File Requirements**
Your CSV file should include these columns:
- `Agent Name` - Name of the call agent
- `Current campaign` - Campaign name
- `Disposition` - Call outcome (Voicemail, Dead Call, etc.)
- `Recording Length (Seconds)` - Call duration
- `Phone Number` - Contact number

### **User Credentials**
Pre-configured users with password `12345resva`:
- Abdo
- Ahmed Hanafy
- destroyer of the galaxy
- el dlo3a
- Nour
- Danial
- Zizi
- Ali

## 📈 Usage Guide

### **1. Login & Upload**
- Login with your credentials
- Upload your call log CSV file
- Wait for data processing

### **2. Apply Filters**
- **Agent Filter**: Select specific agent or "All users"
- **Campaign Filter**: Select specific campaign or "All campaigns"
- Filters work independently for different sections

### **3. Analyze Results**
- **Overall Summary**: View total metrics
- **Agent Summary**: Check individual performance
- **Campaign Summary**: Analyze campaign reachability
- **Flagged Calls**: Review problematic calls

### **4. Export Data**
- Download filtered results as CSV
- Export specific agent or campaign data

## 🎯 Key Features Explained

### **Campaign Reachability Analysis**
The tool automatically analyzes campaign performance by comparing:
- **Low Engagement Calls**: Dead Calls + Unknown + Voicemail
- **Good Engagement Calls**: Decision Maker + Wrong Number

**Results**:
- **Low Reachability**: When low engagement > good engagement
- **Good Reachability**: When good engagement ≥ low engagement

### **Smart Filtering**
- **Agent Filter**: Only affects Flagged Calls section
- **Campaign Filter**: Only affects Campaign Summary section
- **Independent Operation**: Filters don't interfere with each other

## 🚀 Deployment

### **Streamlit Cloud**
1. Push code to GitHub
2. Connect repository to Streamlit Cloud
3. Deploy automatically

### **Heroku**
1. Add `setup.sh` and `Procfile`
2. Deploy using Heroku CLI
3. Configure environment variables

### **Local Deployment**
```bash
streamlit run audit2_app.py --server.port 8501 --server.address 0.0.0.0
```

## 🔒 Security Features

- **Session Management**: Secure login/logout
- **Input Validation**: Data sanitization
- **Error Handling**: Graceful error management
- **Access Control**: User-based authentication

## 📞 Support

For technical support or feature requests, contact:
- **Developer**: Mohamed Abdo
- **Telegram**: [@Mohmed_abdo](https://t.me/Mohmed_abdo)

## 📄 License

© 2025 Mohamed Abdo. All rights reserved.

---

**Developed with ❤️ for professional call center analytics** 