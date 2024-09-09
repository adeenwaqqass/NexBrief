# NexBrief 
### News Aggregator
---
### **Project Overview:**

This application is designed to fetch the latest news articles from various sources, summarize them into 60 words, and present them in a user-friendly, minimalistic interface. It provides users with a quick glance at important news, and upon clicking, redirects them to the original article for full details.

---

### **Tech Stack:**

1. **Frontend**:

   - **Framework**: Vite + React
   - **Styling**: Tailwind CSS
   - **Frontend Components**:
     - **Header**: Displays the logo and key navigation options.
     - **SideNav**: A collapsible side navigation bar that allows users to filter news by categories (sports, technology, finance, etc.) or search by country.
     - **Body**: The main content area where news cards are displayed.
     - **NewsCard**: Each card displays a summarized article with a photo, 60-word summary, and a link to the full article.
   - **User Interaction**:
     - Smooth animations for collapsing/expanding the SideNav.
     - A search bar to filter news.
     - News cards redirect users to the full article from the original source.
2. **Backend**:

   - **Framework**: FastAPI (Python)
   - **News Source**: NewsAPI.org
   - **Summarization**: LangChain for summarizing articles into concise, 60-word summaries.
   - **Backend Features**:
     - API endpoints to fetch news and return summarized articles.
     - Integrates with NewsAPI to fetch articles based on user preferences (genre, country).
     - Uses LangChain to generate concise news summaries before sending them to the frontend.
     - Optional caching layer to optimize performance and reduce API hits.
3. **API Integration**:

   - **NewsAPI.org**:
     - Fetches the latest articles.
     - Provides the ability to filter by category (sports, technology, politics, etc.) and country.
     - Ensures up-to-date news coverage.
4. **Summarization Logic**:

   - **LangChain**:
     - Summarizes lengthy news articles into concise 60-word snippets.
     - Ensures that summaries are informative and cohesive for a better user experience.

---

### **User Flow**:

1. **Landing Page**:

   - The user is greeted with a clean interface showing the latest summarized news articles.
2. **Side Navigation**:

   - Users can expand the collapsible SideNav to filter news by genre or country.
   - When hovered or expanded, the rest of the page blurs, focusing attention on the navigation.
3. **News Cards**:

   - Each news card shows a photo on the left and a 60-word summary on the right.
   - Users can click on the card to be redirected to the full article on the original news source.
   - The page displays 30 cards, with 2 cards per row.
4. **Search & Filters**:

   - Users can search or select genres/countries from the SideNav.
   - The page reloads to display news based on the selected filters.
5. **Backend Interaction**:

   - The frontend sends the user’s search/filter query to the backend via API requests.
   - The backend fetches the news from NewsAPI.org, summarizes it, and returns the summaries to the frontend.
   - Summarized articles are displayed on the frontend in real-time.

---

### **Key Features**:

- **Summarized News**: Get quick 60-word summaries of the latest news across various categories.
- **Interactive SideNav**: Smoothly collapses and expands, allowing easy navigation and filtering of news.
- **News Filtering**: Filter news by category or country using the SideNav.
- **Smooth Animations**: Responsive, fluid user interface powered by Tailwind CSS and React.
- **External Links**: Clicking on a news card redirects users to the original full article.

---

### **Planned Enhancements**:

- **Caching**: Implement a caching mechanism to store news articles temporarily, reducing the need for repeated API calls.
- **Pagination**: Add pagination or infinite scrolling to manage the large number of news cards more effectively.
- **User Authentication**: Optional feature to allow users to save or bookmark news articles.
- **Advanced Summarization**: Experiment with more advanced summarization techniques using LangChain to further improve summary quality.
