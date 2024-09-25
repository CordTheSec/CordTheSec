// Function to create a mod menu in Tribals.io game
function createModMenu() {
    // Define the mod menu elements
    const modMenu = document.createElement('div');
    modMenu.id = 'mod-menu';
    modMenu.style.position = 'fixed';
    modMenu.style.top = '10px';
    modMenu.style.right = '10px';
    modMenu.style.background = 'rgba(255, 255, 255, 0.8)';
    modMenu.style.padding = '10px';
    modMenu.style.border = '1px solid black';
    modMenu.style.borderRadius = '5px';
    modMenu.style.zIndex = '9999';

    // Add mod menu options
    const modOptions = [
        { name: 'God Mode', action: 'EnableGodMode()' },
        { name: 'Unlimited Resources', action: 'EnableUnlimitedResources()' },
        { name: 'Unlock All Levels', action: 'UnlockAllLevels()' }
    ];

    modOptions.forEach(option => {
        const modButton = document.createElement('button');
        modButton.textContent = option.name;
        modButton.onclick = () => eval(option.action); // Using eval for simplicity, can be improved for security
        modMenu.appendChild(modButton);
    });

    // Append mod menu to the document body
    document.body.appendChild(modMenu);
}

// Example Usage
// Call the function to create the mod menu when the page loads
window.onload = function() {
    createModMenu();
};
