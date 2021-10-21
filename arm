#include <stdlib.h>
#include <GL/glut.h>


static int shoulder = 0, elbow = 0, fingerBase = 0, fingerUp = 0;
int moving, startx, starty;


GLfloat angle = 0.0;   /* in degrees */
GLfloat angle2 = 0.0;   /* in degrees */


void init(void)
{
	glClearColor(0.0, 0.0, 0.0, 0.0);
	glShadeModel(GL_FLAT);
}

void display(void)
{
	glClear(GL_COLOR_BUFFER_BIT);
	glPushMatrix(); //stack: [I]
	glRotatef(angle2, 1.0, 0.0, 0.0);
	glRotatef(angle, 0.0, 1.0, 0.0);
	glTranslatef(-1.0, 0.0, 0.0);
	glRotatef((GLfloat)shoulder, 0.0, 0.0, 1.0);
	glTranslatef(1.0, 0.0, 0.0);
	glPushMatrix(); //stack: [RRTRT][I]
	glScalef(2.0, 0.6, 1.0);
	glutWireCube(1.0);
	glPopMatrix(); //stack: [I]
	glTranslatef(1.0, 0.0, 0.0);
	glRotatef((GLfloat)elbow, 0.0, 0.0, 1.0);
	glTranslatef(1.0, 0.0, 0.0);
	glPushMatrix(); //stack: [TRT][I]
	glPushMatrix(); //stack: [TRT][TRT][I]
	glScalef(2.0, 0.6, 1.0);
	glutWireCube(1.0);
	glPopMatrix(); //stack: [TRT][I] // CM: [TRT] 

	////Draw finger1 flange1 
	//glTranslatef(1.0, -0.2, 0.3);
	//glRotatef((GLfloat)fingerBase, 0.0, 0.0, 1.0);
	//glTranslatef(0.15, 0.0, 0.0);
	//glPushMatrix(); // stack: [TRT]'[TRT][I]
	//glScalef(0.3, 0.1, 0.1);
	//glPushMatrix(); // stack: [TRTS][TRT]'[TRT][I]
	//glutWireCube(1);
	//glPopMatrix(); // stack: [TRT]'[I] // CM: [TRTS]

	//Draw finger1 flange1 
	glTranslatef(1.0, -0.2, 0.2);
	glRotatef((GLfloat)fingerBase, 0.0, 0.0, 1.0);
	glTranslatef(0.15, 0.0, 0.0);
	glPushMatrix(); // stack: [TRT]'[TRT][I]
	glScalef(0.3, 0.1, 0.1);
	glutWireCube(1);
	glPopMatrix(); // stack: [TRT][I] // CM: [TRT]'

	//Draw finger1 flange2
	glTranslatef(0.15, 0.0, 0.0);
	glRotatef((GLfloat)fingerUp, 0.0, 0.0, 1.0);
	glTranslatef(0.15, 0.0, 0.0);
	//glPushMatrix(); // stack: [TRT]"[TRT]'[I]
	glScalef(0.3, 0.1, 0.1);
	glutWireCube(1);
	//glPopMatrix(); // stack: [TRT]'[I] // CM: [TRT]"
	glPopMatrix(); // stack: [I] // CM: [TRT]
	glPushMatrix(); // stack: [TRT][I] // CM: [TRT]


	//Draw finger2 flange1 
	glTranslatef(1.0, 0.2, 0.3);
	glRotatef((GLfloat)fingerBase, 0.0, 0.0, -1.0);
	glTranslatef(0.15, 0.0, 0.0);
	glPushMatrix(); // stack: [TRT]'[TRT][I]
	glScalef(0.3, 0.1, 0.1);
	glutWireCube(1);
	glPopMatrix(); // stack: [TRT][I] // CM: [TRT]'

	//Draw finger2 flange2
	glTranslatef(0.15, 0.0, 0.0);
	glRotatef((GLfloat)fingerUp, 0.0, 0.0, -1.0);
	glTranslatef(0.15, 0.0, 0.0);
	//glPushMatrix(); 
	glScalef(0.3, 0.1, 0.1);
	glutWireCube(1);
	//glPopMatrix(); 
	glPopMatrix(); // stack: [I] // CM: [TRT]
	glPushMatrix(); // stack: [TRT][I] // CM: [TRT]

	//Draw finger3 flange1 
	glTranslatef(1.0, 0.2, 0.1);
	glRotatef((GLfloat)fingerBase, 0.0, 0.0, -1.0);
	glTranslatef(0.15, 0.0, 0.0);
	glPushMatrix(); // stack: [TRT]'[TRT][I]
	glScalef(0.3, 0.1, 0.1);
	glutWireCube(1);
	glPopMatrix(); // stack: [TRT]'[I] // CM: [TRTS]

	//Draw finger3 flange2
	glTranslatef(0.15, 0.0, 0.0);
	glRotatef((GLfloat)fingerUp, 0.0, 0.0, -1.0);
	glTranslatef(0.15, 0.0, 0.0);
	//glPushMatrix(); 
	glScalef(0.3, 0.1, 0.1);
	glutWireCube(1);
	//glPopMatrix(); 
	glPopMatrix();
	glPushMatrix();

	//Draw finger4 flange1 
	glTranslatef(1.0, 0.2, -0.1);
	glRotatef((GLfloat)fingerBase, 0.0, 0.0, -1.0);
	glTranslatef(0.15, 0.0, 0.0);
	glPushMatrix(); // stack: [TRT]'[TRT][I]
	glScalef(0.3, 0.1, 0.1);
	glutWireCube(1);
	glPopMatrix(); // stack: [TRT]'[I] // CM: [TRTS]

	//Draw finger4 flange2
	glTranslatef(0.15, 0.0, 0.0);
	glRotatef((GLfloat)fingerUp, 0.0, 0.0, -1.0);
	glTranslatef(0.15, 0.0, 0.0);
	//glPushMatrix(); 
	glScalef(0.3, 0.1, 0.1);
	glutWireCube(1);
	//glPopMatrix(); 
	glPopMatrix();
	glPushMatrix();

	//Draw finger5 flange1 
	glTranslatef(1.0, 0.2, -0.3);
	glRotatef((GLfloat)fingerBase, 0.0, 0.0, -1.0);
	glTranslatef(0.15, 0.0, 0.0);
	glPushMatrix(); // stack: [TRT]'[TRT][I]
	glScalef(0.3, 0.1, 0.1);
	glutWireCube(1);
	glPopMatrix(); // stack: [TRT]'[I] // CM: [TRTS]

	//Draw finger5 flange2
	glTranslatef(0.15, 0.0, 0.0);
	glRotatef((GLfloat)fingerUp, 0.0, 0.0, -1.0);
	glTranslatef(0.15, 0.0, 0.0);
	//glPushMatrix(); 
	glScalef(0.3, 0.1, 0.1);
	glutWireCube(1);
	//glPopMatrix(); 
	glPopMatrix();
	glPushMatrix();
	
	
	
	glPopMatrix();
	

	////Draw finger2 flange1 
	//glTranslatef(1.0, 0.2, 0.3);
	//glRotatef((GLfloat)fingerBase, 0.0, 0.0, 1.0);
	//glTranslatef(0.15, 0.0, 0.0);
	//glPushMatrix();
	//glScalef(0.3, 0.1, 0.1);
	//glutWireCube(1);
	//glPopMatrix();

	////Draw finger2 flange2
	//glTranslatef(0.15, 0.0, 0.0);
	//glRotatef((GLfloat)fingerUp, 0.0, 0.0, 1.0);
	//glTranslatef(0.15, 0.0, 0.0);
	//glPushMatrix();
	//glScalef(0.3, 0.1, 0.1);
	//glutWireCube(1);
	//glPopMatrix();
	

	glPopMatrix();
	glutSwapBuffers();
}

void reshape(int w, int h)
{
	glViewport(0, 0, (GLsizei)w, (GLsizei)h);
	glMatrixMode(GL_PROJECTION);
	glLoadIdentity();
	gluPerspective(85.0, (GLfloat)w / (GLfloat)h, 1.0, 20.0);
	glMatrixMode(GL_MODELVIEW);
	glLoadIdentity();
	glTranslatef(0.0, 0.0, -5.0);
}

void keyboard(unsigned char key, int x, int y)
{
	switch (key)
	{
	case 's':
		shoulder = (shoulder + 5) % 360;
		glutPostRedisplay();
		break;
	case 'S':
		shoulder = (shoulder - 5) % 360;
		glutPostRedisplay();
		break;
	case 'e':
		elbow = (elbow + 5) % 360;
		glutPostRedisplay();
		break;
	case 'E':
		elbow = (elbow - 5) % 360;
		glutPostRedisplay();
		break;
	case 'f':
		fingerBase = (fingerBase + 5) % 360;
		glutPostRedisplay();
		break;
	case 'F':
		fingerBase = (fingerBase - 5) % 360;
		glutPostRedisplay();
		break;
	case 'g':
		fingerUp = (fingerUp + 5) % 360;
		glutPostRedisplay();
		break;
	case 'G':
		fingerUp = (fingerUp - 5) % 360;
		glutPostRedisplay();
		break;

	case 27:
		exit(0);
		break;
	default:
		break;
	}
}

static void mouse(int button, int state, int x, int y)
{
	if (button == GLUT_LEFT_BUTTON) {
		if (state == GLUT_DOWN) {
			moving = 1;
			startx = x;
			starty = y;
		}
		if (state == GLUT_UP) {
			moving = 0;
		}
	}
}


static void motion(int x, int y)
{
	if (moving) {
		angle = angle + (x - startx);
		angle2 = angle2 + (y - starty);
		startx = x;
		starty = y;
		glutPostRedisplay();
	}
}



int main(int argc, char **argv)
{
	glutInit(&argc, argv);
	glutInitDisplayMode(GLUT_DOUBLE | GLUT_RGB);
	glutInitWindowSize(500, 500);
	glutInitWindowPosition(100, 100);
	glutCreateWindow(argv[0]);
	init();
	glutMouseFunc(mouse);
	glutMotionFunc(motion);
	glutDisplayFunc(display);
	glutReshapeFunc(reshape);
	glutKeyboardFunc(keyboard);
	glutMainLoop();
	return 0;
}
