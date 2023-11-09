## NOTES ABOUT THE ALGORITHM
**functions used

- 1 - char	*get_next_line(int fd)
Get as parameter the number file descriptor and returns the line.

- 2 - char	*get_text(int fd, char	*buffer)
    Get as paramether the file descriptor.
    Returns the text of the line, including if we found more after the \n.

- 3 - char	*get_only_line(char	*buffer)
    Receive as a paramether the text that we got with get_text().
    Allocates memory for the line using ft_strlen modified to get the len until \n.
    returns the line until \n.

- 4 - get_after_n(char *buffer)
    Receive as a paramether the text the got with get_only_line();
    and returns a char with the characters after \n.

**We have subfunctions here as well, but i will analize this after**

char	*get_next_line(int fd)
{
	static char	*buffer;
	char		*line;

	if (fd < 0 || BUFFER_SIZE <= 0)
		return (NULL);
	buffer = get_text(fd, buffer);
	if (!buffer)
	{
		free(buffer);
		return (NULL);
	}
	line = get_only_line(buffer);
	buffer = get_after_n(buffer);
	return (line);
}