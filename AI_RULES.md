# AI Rules for PrecastPro Application

This document outlines the core technologies used in the PrecastPro application and provides guidelines for their usage to ensure consistency, maintainability, and adherence to best practices.

## Tech Stack Overview

*   **Frontend Framework**: React
*   **Language**: TypeScript
*   **Styling**: Tailwind CSS
*   **UI Component Library**: shadcn/ui (built on Radix UI)
*   **Routing**: React Router
*   **Icons**: Lucide-react, Material Symbols Outlined
*   **Fonts**: Google Fonts (Manrope, Noto Sans)
*   **Build Tool**: Vite (implied by project structure)
*   **Project Structure**: Components in `src/components/`, pages in `src/pages/`, main page `src/pages/Index.tsx`, routes in `src/App.tsx`.

## Library Usage Rules

*   **React**: All user interface components and application logic must be built using React.
*   **TypeScript**: All new code and modifications should be written in TypeScript to leverage type safety and improve code quality.
*   **Tailwind CSS**: Use Tailwind CSS exclusively for all styling. Avoid inline styles or separate CSS files unless absolutely necessary and explicitly approved.
*   **shadcn/ui**: Prioritize using pre-built components from the shadcn/ui library for common UI elements (e.g., buttons, forms, cards, dialogs). Do not modify the source files of shadcn/ui components directly; if customization is needed, create a new component that wraps or extends the shadcn/ui component.
*   **React Router**: Implement all client-side navigation and routing using React Router. Keep the main route definitions within `src/App.tsx`.
*   **Lucide-react**: Use icons from the `lucide-react` package.
*   **Material Symbols Outlined**: Can be used for additional icons if a suitable option is not available in `lucide-react`.
*   **No other UI libraries**: Do not introduce other UI component libraries. Stick to shadcn/ui for consistency.
*   **No direct DOM manipulation**: Avoid direct DOM manipulation (e.g., using `document.getElementById`) as it goes against React's declarative paradigm.
*   **Responsive Design**: Always ensure designs are responsive and work well across various screen sizes.
*   **Toasts**: Use toast notifications (e.g., `react-hot-toast` if installed) to inform users about important events.
*   **Error Handling**: Do not implement `try/catch` blocks for error handling unless specifically requested. Errors should bubble up for central management.