
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

        É uma família definidas pelo IEEE para manutenção e compatibilidade entre os sistemas operacionais.

3. Considerando a norma POSIX, responda:

(a) Quais são as funções (e seus protótipos) para abrir e fechar arquivos?

(b) Quais são as funções (e seus protótipos) para escrever em arquivos?

(c) Quais são as funções (e seus protótipos) para ler arquivos?

(d) Quais são as funções (e seus protótipos) para reposicionar um ponteiro para arquivo?

(e) Quais bibliotecas devem ser incluídas no código para poder utilizar as funções acima?
