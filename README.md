# AI Agent

A modern, AI-powered chat assistant built with Next.js, React, and TypeScript. AI Agent provides an elegant interface for interacting with multiple AI models through OpenRouter, with support for knowledge base integration, streaming responses, and advanced chat management features.

## ✨ Features

- 🤖 **Multiple AI Models**: Choose from various free and premium AI models including Llama 3.3, DeepSeek R1, Devstral 2, and more
- 📚 **Knowledge Base Integration**: Automatically loads and uses knowledge from markdown/text files in the `content/` directory
- 💬 **Streaming Responses**: Real-time streaming of AI responses for a smooth, ChatGPT-like experience
- 🎨 **Beautiful UI**: Modern dark-themed interface with glassmorphism effects and smooth animations
- 📝 **Chat Management**: 
  - Multiple chat sessions with persistent storage
  - Edit and regenerate messages
  - Export conversations as markdown files
  - Copy messages to clipboard
- ⚙️ **Advanced Settings**:
  - Adjustable temperature (0-2) for response creativity
  - Custom system prompts for personalized AI behavior
  - Model selection dropdown
- 🔄 **Message Features**:
  - Edit user messages and regenerate AI responses
  - Regenerate AI responses on demand
  - AI-powered prompt improvement
- 💾 **Local Storage**: All chats and settings are saved locally in your browser

## 🚀 Getting Started

### Prerequisites

- Node.js 18+ and npm/yarn/pnpm
- An OpenRouter API key ([Get one here](https://openrouter.ai/))

### Installation

1. **Clone the repository**
   ```bash
   git clone https://github.com/yourusername/ai-agent.git
   cd ai-agent
   ```

2. **Install dependencies**
   ```bash
   npm install
   # or
   yarn install
   # or
   pnpm install
   ```

3. **Set up environment variables**
   
   Create a `.env.local` file in the root directory:
   ```env
   OPENROUTER_API_KEY=your_openrouter_api_key_here
   NEXT_PUBLIC_SITE_URL=http://localhost:3000
   ```

4. **Add your knowledge base** (Optional)
   
   Create a `content/` directory in the root and add your markdown or text files:
   ```
   content/
     ├── knowledge.md
     ├── documentation.txt
     └── ...
   ```

5. **Run the development server**
   ```bash
   npm run dev
   # or
   yarn dev
   # or
   pnpm dev
   ```

6. **Open your browser**
   
   Navigate to [http://localhost:3000](http://localhost:3000)

## 📖 Usage

1. **Start a Conversation**: Type your message in the input field and press Enter
2. **Select AI Model**: Click the model selector in the top bar to choose from available models
3. **Manage Chats**: Use the sidebar to create new chats, switch between sessions, or delete old ones
4. **Customize Settings**: Click the settings icon to adjust temperature and add custom system prompts
5. **Edit Messages**: Hover over a user message and click the edit icon to modify and regenerate
6. **Export Chats**: Click the download icon to export your conversation as a markdown file

## 🛠️ Tech Stack

- **Framework**: [Next.js 15](https://nextjs.org/) with App Router
- **Language**: [TypeScript](https://www.typescriptlang.org/)
- **UI Library**: [React 19](https://react.dev/)
- **Styling**: [Tailwind CSS](https://tailwindcss.com/)
- **UI Components**: [Radix UI](https://www.radix-ui.com/)
- **Markdown Rendering**: [react-markdown](https://github.com/remarkjs/react-markdown)
- **Icons**: [Lucide React](https://lucide.dev/)
- **AI Integration**: [OpenRouter API](https://openrouter.ai/)

## 📁 Project Structure

```
ai-agent/
├── app/
│   ├── api/
│   │   └── chat/
│   │       ├── route.ts          # Non-streaming chat endpoint
│   │       └── stream/
│   │           └── route.ts      # Streaming chat endpoint
│   ├── layout.tsx                 # Root layout
│   ├── page.tsx                   # Home page
│   └── globals.css                # Global styles
├── components/
│   ├── chat-interface.tsx         # Main chat component
│   ├── chat-sidebar.tsx           # Sidebar for chat sessions
│   ├── mermaid.tsx                # Code block component
│   └── ui/
│       └── button.tsx             # Button component
├── lib/
│   └── utils.ts                   # Utility functions
├── content/                       # Knowledge base files (create this)
│   └── knowledge.md
└── public/                        # Static assets
```

## 🔧 Configuration

### Available AI Models

The application supports multiple AI models from OpenRouter. Free tier models include:

- **Mimo V2 Flash** (Xiaomi) - Default, fast and efficient
- **Llama 3.3 70B** (Meta) - Powerful and versatile
- **Devstral 2** (Mistral) - Great for coding tasks
- **DeepSeek R1** (DeepSeek) - Advanced reasoning
- **GLM 4.5 Air** (Z.AI) - Lightweight and fast

You can modify the available models in `components/chat-interface.tsx`.

### Environment Variables

| Variable | Description | Required |
|----------|-------------|----------|
| `OPENROUTER_API_KEY` | Your OpenRouter API key | Yes |
| `NEXT_PUBLIC_SITE_URL` | Your site URL (for API headers) | Optional |

## 🎨 Customization

### Styling

The app uses Tailwind CSS with a custom dark theme. You can modify colors and styles in:
- `app/globals.css` - Global styles and CSS variables
- `tailwind.config.ts` - Tailwind configuration


