# 42Cursus_libft
primer ejercicio del curso 42
<p>leaks<p>
  void leaks(void)
{
	system("leaks -q a.out");
}

int main()
{
	char  **sp;
	size_t i = 0;
	char cad[] = "hola separador  de espacio  ";
	sp = ft_split(cad, ' ');
	char *prueba;

	while(i < 4)
	{
		prueba = sp[i];
		printf("PR: %s\n", prueba);
		free(prueba);
		i++;
	}
	free(sp);
	//atexit(leaks);
	//system("leaks -q a.out");
}

<p>testers<p>

https://github.com/alelievr/libft-unit-test escudos
https://github.com/Tripouille/libftTester tripouille
		
		
#include <stdio.h>
#include <unistd.h>
#include <fcntl.h>
#include <limits.h>
int main()
{
	static char *tem;
	int fd;
	char buf;
	ssize_t nr_bytes;
	fd = open("/Users/jporta/Desktop/pepe.txt", O_RDONLY);

	if (fd == -1)
		printf("error al leer archivo");
	else
	{
		nr_bytes = read (fd, buf, BUFFER_SIZE);
		close(fd);

		if (nr_bytes == 0)
		{
			printf("archivo vacio \n");
		}
		else 
		{
			
			printf("el numero de caracteres es %d, contenido es\n%s", (int)nr_bytes, buf);
		}
	}
	return (0);
}#include <stdio.h>
#include <unistd.h>
#include <fcntl.h>
#include <limits.h>
int main()
{
	static char *tem;
	int fd;
	char buf;
	ssize_t nr_bytes;
	fd = open("/Users/jporta/Desktop/pepe.txt", O_RDONLY);

	if (fd == -1)
		printf("error al leer archivo");
	else
	{
		nr_bytes = read (fd, buf, BUFFER_SIZE);
		close(fd);

		if (nr_bytes == 0)
		{
			printf("archivo vacio \n");
		}
		else 
		{
			
			printf("el numero de caracteres es %d, contenido es\n%s", (int)nr_bytes, buf);
		}
	}
	return (0);
}
