<!-- ================= HERO HEADER: Full Width Waving Box ================= -->
<p align="center" style="margin:0;padding:0;">
  <img src="https://capsule-render.vercel.app/api?type=waving&animation=fadeIn&color=gradient&height=110&section=header&text=Hi,+I'm+M.D.+SAKIBUL+ISLAM+SHOVON&fontSize=28&fontAlignY=38" alt="Shovon Name Animation" />
</p>

<!-- ================= SEQUENTIAL MULTI-LINE TYPING ================= -->
<p align="center" style="margin:0;padding:0;">
  <img src="https://readme-typing-svg.demolab.com?font=Fira+Code&weight=600&size=20&duration=3500&pause=800&color=58A6FF&center=true&vCenter=true&width=450&lines=Welcome%20to%20my%20GitHub%20profile!;A%20passionate%20frontend%20developer;Always%20learning%20new%20things;Problem%20Solver;%20Building%20Clean%20and%20Scalable%20Code;Frontend%20%7C%7C%20Web%20Developer" alt="Fast Typing Animation" />
</p>


<!-- ================= CODING GIF (RIGHT SIDE) ================= -->

<img align="right" width="210" src="https://media.giphy.com/media/qgQUggAC3Pfv687qPC/giphy.gif" />



<!-- ================= ABOUT ME SECTION (Static, Extra Compact) ================= -->

<p align="left">
  <img src="https://img.shields.io/badge/B.Sc._Engg._in_CSE-FF5733?style=flat&logo=googlescholar&logoColor=white"
       style="height:26px; transform: scale(1.05); margin-right:5px;" />
  <img src="https://img.shields.io/badge/Patuakhali Science and Technology University-006400?style=flat&logo=google-earth&logoColor=white"
       style="height:26px; transform: scale(1.05);" />
</p>



<!-- ========================================================= -->
<!-- ==================== SOCIAL LINKS ====================== -->
<!-- ========================================================= -->
<p align="left">
  <a href="https://facebook.com/sakibul944" target="_blank">
    <img src="https://img.shields.io/badge/Facebook-1877F2?style=for-the-badge&logo=facebook&logoColor=white" alt="Facebook" />
  </a>
  <a href="https://linkedin.com/in/md-si-shovon" target="_blank">
    <img src="https://img.shields.io/badge/LinkedIn-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white" alt="LinkedIn" />
  </a>
  <a href="mailto:sakibul944@gmail.com">
    <img src="https://img.shields.io/badge/Email-EA4335?style=for-the-badge&logo=gmail&logoColor=white" alt="Email" />
  </a>
</p>


<!-- ================= SKILLS / TECH STACK ICONS (One Line) ================= -->
<p>
  <img src="https://skillicons.dev/icons?i=c,cpp,java,python,html,css,git,github&theme=dark" />
  <img src="https://img.shields.io/badge/Focusing_on-Data_Structures_&_Algorithms-FFD700?style=for-the-badge&logo=codeforces&logoColor=black" />
</p>




<!-- ================= CONTRIBUTION SNAKE ANIMATION ================= -->

<p align="center">
  <img src="https://raw.githubusercontent.com/Platane/snk/output/github-contribution-grid-snake-dark.svg" />
</p>












### 🌌 My Custom Particle Animation (Pygame)

import pygame
import random
import math

# Initial Settings
pygame.init()
WIDTH, HEIGHT = 800, 600
screen = pygame.display.set_mode((WIDTH, HEIGHT))
pygame.display.set_caption("Particle Network")

# Colors & Config
BLACK = (0, 0, 0)
WHITE = (255, 255, 255)
NUM_PARTICLES = 100
MAX_DISTANCE = 100

class Particle:
    def __init__(self):
        self.x = random.randint(0, WIDTH)
        self.y = random.randint(0, HEIGHT)
        self.vx = random.uniform(-1, 1)
        self.vy = random.uniform(-1, 1)

    def move(self):
        self.x += self.vx
        self.y += self.vy
        if self.x <= 0 or self.x >= WIDTH: self.vx *= -1
        if self.y <= 0 or self.y >= HEIGHT: self.vy *= -1

    def draw(self):
        pygame.draw.circle(screen, WHITE, (int(self.x), int(self.y)), 2)

particles = [Particle() for _ in range(NUM_PARTICLES)]

def draw_lines():
    mouse_pos = pygame.mouse.get_pos()
    for i in range(len(particles)):
        p1 = particles[i]
        
        # Mouse attraction logic
        dx_m, dy_m = mouse_pos[0] - p1.x, mouse_pos[1] - p1.y
        dist_m = math.hypot(dx_m, dy_m)
        if dist_m < 150:
            p1.x += dx_m * 0.02
            p1.y += dy_m * 0.02

        for j in range(i + 1, len(particles)):
            p2 = particles[j]
            dist = math.hypot(p1.x - p2.x, p1.y - p2.y)
            if dist < MAX_DISTANCE:
                alpha = int(255 * (1 - dist / MAX_DISTANCE))
                pygame.draw.line(screen, (alpha, alpha, alpha), (p1.x, p1.y), (p2.x, p2.y), 1)

# Main Loop
running = True
clock = pygame.time.Clock()
while running:
    screen.fill(BLACK)
    for event in pygame.event.get():
        if event.type == pygame.QUIT: running = False

    for p in particles:
        p.move()
        p.draw()
    draw_lines()
    pygame.display.flip()
    clock.tick(60)

pygame.quit()













<!-- ================= RANDOM QUOTE ================= -->

<p align="center">
  <img src="https://quotes-github-readme.vercel.app/api?type=horizontal&theme=dark" />
</p>



<!-- ================= PROFILE VIEW COUNTER ================= -->

<p align="center">
  <img src="https://komarev.com/ghpvc/?username=SHOVON944&label=Profile%20views&color=0e75b6&style=flat" />
</p>


<!-- ================= FOOTER THANK YOU LINE ================= -->
<p align="center">
  <img src="https://readme-typing-svg.demolab.com?font=Fira+Code&weight=600&size=18&pause=1000&color=58A6FF&center=true&vCenter=true&width=500&lines=Thanks%20for%20visiting%20my%20GitHub%20profile!;Your%20support%20means%20a%20lot;Stay%20tuned%20for%20more%20projects;Let's%20build%20something%20awesome%20together" alt="Footer Typing Animation" />
</p>





