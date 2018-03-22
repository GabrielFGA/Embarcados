
1. Considerando a biblioteca-padrão da linguagem C, responda:

(a) Quais são as funções (e seus protótipos) para abrir e fechar arquivos?

    para abrir o arquivo: fopen.
        FILE *fopen(const char *file_name, const char *mode);
    para fechar o arquivo: fclose.
        FILE *fclose(FILE *stream);

(b) Quais são as funções (e seus protótipos) para escrever em arquivos?

    size_t fwrite(void *ptr, size_t variavel, size_t quantidadeelementos, FILE *stream);

(c) Quais são as funções (e seus protótipos) para ler arquivos?

    size_t fread(void *ptr, size_t variavel, size_t quantidadeelementos, FILE* stream);

(d) Quais são as funções (e seus protótipos) para reposicionar um ponteiro para arquivo?

    int fseek(FILE *stream, long int offset, int whence);
    
    whence pode ser: SEEK_SET, SEEK_CRU, SEEK_END.

(e) Quais bibliotecas devem ser incluídas no código para poder utilizar as funções acima?

    Uma das bibliotecas padrão de C: stdio.h

2. O que é a norma POSIX?

       É uma família de normas definidas pelo IEEE para manutenção e compatibilidade entre os sistemas operacionais.

3. Considerando a norma POSIX, responda:

(a) Quais são as funções (e seus protótipos) para abrir e fechar arquivos?

    Para abrir, se utiliza a função open:
        int open(const char *path, int flag); 
        //onde path é o caminho e flag é o modo de abertura (O_WRONLY, O_RDONLY, O_RDWR...).
    Para fechar, se utiliza a função close:
        int close(int fildes);
        
(b) Quais são as funções (e seus protótipos) para escrever em arquivos?

    Para escrever é utilizada afunção write:
        ssize_t write(int fildes, const void *buf, size_t bytes);

(c) Quais são as funções (e seus protótipos) para ler arquivos?

    Para ler, utiliza-se read:
        ssize_t read(int fildes, void *buf, seize_t bytes);

(d) Quais são as funções (e seus protótipos) para reposicionar um ponteiro para arquivo?

    a função utilizada pra reposicionar um ponteiro para arquivo é a lseek:
        off_t lseek(int fildes, off_t offset, int whence);
        \\onde whence pode ser: SEEK_SET, SEEK_CUR ou SEEK_END.

(e) Quais bibliotecas devem ser incluídas no código para poder utilizar as funções acima?

    #include <fcntl.h>
    #include <unistd.h>
