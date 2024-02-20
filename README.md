import pygame

# Initialize Pygame
pygame.init()

# Set window size and title
WIDTH, HEIGHT = 800, 600
window = pygame.display.set_mode((WIDTH, HEIGHT))
pygame.display.set_caption("Drawing Shapes")

# Set colors
WHITE = (255, 255, 255)
BLACK = (0, 0, 0)
RED = (255, 0, 0)
GREEN = (0, 255, 0)
BLUE = (0, 0, 255)

# Define shapes (x, y, width, height, color)
shapes = [
    (100, 100, 50, 50, RED),
    (200, 200, 100, 50, GREEN),
    (300, 300, 50, 100, BLUE)
]

# Main loop
running = True
while running:
    for event in pygame.event.get():
        if event.type == pygame.QUIT:
            running = False

    # Draw shapes
    window.fill(WHITE)
    for shape in shapes:
        pygame.draw.rect(window, shape[4], shape[:4])

    # Update display
    pygame.display.update()

# Quit the game
pygame.quit()
