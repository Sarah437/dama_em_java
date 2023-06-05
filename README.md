packag de dados {
public class Posicao {
 private char x;
 private int y;
 //É responsável por mostrar x - linha e com letra e y - números.
 public Posicao() {
 this.x = 'a';
 this.y = 1;
 }
 public Posicao(char x, int y) {
 this.x = x;
 this.y = y;
 }
 @Override
 public String toString() {
 return "" + x + y;
 }
 public char getX() {
 return x;
 }
 public int getY() {
 return y;
 }
 public void setX(char x) {
 this.x = x;
 }
 public void setY(int y) {
 this.y = y;
 }
}
// segunda classe 

public class Peca {
 private String nome;
 private Posicao posicao;
 // Responsável pelo nome e posição da peça.
 public Peca(String nome, Posicao posicao) {
 this.nome = nome;
 this.posicao = posicao;
 }
 public String getNome() {
 return nome;
 }
 public void setNome(String nome) {
 this.nome = nome;
 }
 public Posicao getPosicao() {
 return posicao;
 }
 public void setPosicao(Posicao posicao) {
 this.posicao = posicao;
 }
}

public class Tabuleiro {
 // Criando o Tabuleiro
 public char[][] matriz;
 // Tamanho do tabuleiro
 public static final int TAMANHO = 9;
 private Peca peca;
 //Percorrendo sobre a matriz no caso pelo "Tabuleiro", assim o Local vazio e preenchida com
" - "
 public Tabuleiro() {
 matriz = new char[TAMANHO][TAMANHO];
 for (int i = 0; i < TAMANHO; i++) {
 for (int j = 0; j < TAMANHO; j++) {
 matriz[i][j] = '-';
 }
 }
 }
 //Imprimindo o Tabuleiro com letras informando linha e numero colunas.
 public void imprimirTabuleiro() {
 System.out.println("\n a b c d e f g ");
 System.out.println("");
 for (int linha = TAMANHO - 2; linha > 0; linha--) {
 System.out.print(" " + linha + " ");
 for (int coluna = 1; coluna < TAMANHO - 1; coluna++) {
 System.out.print(" " + matriz[linha][coluna]);
 }
 System.out.println();
 }
 System.out.println("\n a b c d e f g ");
 }
 public void colocarPecaNoTabuleiro() {
 // Preenchendo fileira 1 e 2
 for (int i = 1; i < TAMANHO - 1; i++) {
 matriz[1][i] = 'J';
 matriz[2][i] = 'J';
 }
 // Preenchendo fileira 7 e 6
 for (int i = 1; i < TAMANHO - 1; i++) {
 matriz[7][i] = 'J';
 matriz[6][i] = 'J';
 }
 }
 public void movimento(int movimento) {
 // Método de movimento da peça no tabuleiro.
 }
}
