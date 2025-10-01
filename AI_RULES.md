# AI_RULES.md

This document outlines the technical stack and development guidelines for this application, intended for AI assistants to ensure consistency and best practices.

## Tech Stack Overview

*   **Frontend Framework**: Vue 3 (Composition API is preferred for new components).
*   **Routing**: Vue Router for client-side navigation.
*   **State Management**: Pinia for centralized application state.
*   **Styling**: Tailwind CSS for utility-first styling, complemented by Sass for pre-processing.
*   **Internationalization**: Vue I18n for multi-language support.
*   **Build Tool**: Vite for development and production builds.
*   **Date & Time Handling**: `date-fns` for all date manipulation and formatting.
*   **Calendar Parsing**: `ical.js` for parsing ICS calendar files.
*   **DOS Emulation**: `js-dos` for running DOS applications within the browser.
*   **Email Functionality**: `emailjs-com` for client-side email sending.
*   **HTTP Client**: `axios` for making API requests.
*   **Meta Tag Management**: `@vueuse/head` for dynamic meta tag updates.
*   **Testing**: Nightwatch.js for end-to-end testing.
*   **Language**: While the current codebase is primarily JavaScript, new files should ideally use TypeScript (`.ts`, `.tsx`, or `<script lang="ts">` in Vue files).

## Library Usage Guidelines

*   **Frontend Development**: All new features and components must be built using Vue 3.
*   **Routing**: Use Vue Router for all client-side navigation. Keep route definitions organized within `src/router/index.js`.
*   **State Management**: Pinia is the designated store for all application-wide state. Create new stores in `src/stores/` as needed.
*   **Styling**: Prioritize Tailwind CSS utility classes for styling. Sass can be used for global styles, variables, or complex nested structures, but prefer Tailwind for component-specific styling.
*   **UI Components**: The `shadcn/ui` library is available. If UI components are needed, `shadcn/ui` should be the first choice. These components should be used as-is; if extensive customization is required, create a new wrapper component in `src/components/` that utilizes the `shadcn/ui` component.
*   **Internationalization**: All user-facing text must be managed through Vue I18n, with locale definitions located in `src/locales/`.
*   **Date & Time**: Use `date-fns` for any operations involving dates or times.
*   **HTTP Requests**: Use `axios` for all HTTP client-side requests.
*   **Icons**: For icons, prefer SVG assets or a Vue-compatible icon library if one is introduced. Avoid `lucide-react` as this is a Vue application.
*   **File Structure**:
    *   New pages should be placed in `src/pages/`.
    *   New components should be placed in `src/components/`.
    *   Each new component or hook must reside in its own dedicated file.
    *   Directory names must be all lower-case (e.g., `src/pages`, `src/components`).

## General Development Guidelines

*   **Responsiveness**: Always generate responsive designs that adapt well to different screen sizes.
*   **Toasts**: Use toast components to inform the user about important events or feedback.
*   **Error Handling**: Do not implement `try/catch` blocks unless specifically requested by the user. Errors should be allowed to bubble up for easier debugging and resolution.
*   **Completeness**: All implemented features must be fully functional with complete code. Avoid placeholders, partial implementations, or `TODO` comments.
*   **Simplicity**: Prioritize simple and elegant solutions. Avoid over-engineering.
*   **Scope**: Only make changes directly requested by the user. Do not add extra features beyond the explicit request.
*   **Code Formatting**: Adhere strictly to the existing code style and conventions.