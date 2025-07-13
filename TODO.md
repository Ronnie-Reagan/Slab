# Wiki and Code Refactor Plan

Below is a proposed list of tasks for migrating documentation to a GitHub Pages powered wiki and for upcoming refactors.

## GitHub Pages Wiki Tasks
1. **Create docs directory** *(done)*
   - Add `docs/index.md` with project overview, quick start, and link to examples.
   - Configure the repository to use the `docs/` folder for GitHub Pages in repository settings.
2. **Migrate existing README content** *(in progress)*
   - Split longer sections (usage, license, credits) into dedicated pages.
   - Keep a trimmed README that links to the wiki.
3. **Write API reference** *(partial)*
   - Document each module and function from `API.lua`.
   - Include code snippets and images from `SlabTest.lua`.
4. **Add tutorials and examples**
   - Show how to set up the library, draw basic windows, and use controls.
   - Include a page for common patterns (dialogs, docking, debug tools).
5. **Add contribution guidelines and FAQ**
   - Explain how to run demos and where to report issues.
6. **Publish and verify**
   - Enable GitHub Pages, check links, and verify rendering on mobile and desktop.

## Refactor Tasks
1. **Adopt lower camel case naming**
   - Convert all public API functions (e.g. `Slab.Initialize` -> `Slab.initialize`).
   - Update internal modules and examples accordingly.
   - Maintain backward compatibility with deprecated names temporarily.
2. **Introduce window classes**
   - Create a `Window` class that encapsulates title, position, and size.
   - Store window instances outside the `love.update` loop in `main.lua`.
   - Provide methods like `update`, `draw`, `toggle`, and `isOpen`.
3. **Refactor example application**
   - Rewrite `main.lua` to predefine windows and call their methods inside `love.update` and `love.draw`.
   - Demonstrate object usage in `SlabTest.lua`.
4. **Update documentation**
   - Reflect naming changes and new OOP usage in the wiki.
5. **Future improvements**
   - Review remaining TODO items in `changelog.txt` and prioritize them after the refactor.
