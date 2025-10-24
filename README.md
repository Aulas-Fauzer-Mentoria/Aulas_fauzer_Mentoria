import java.util.List;
import java.util.stream.Collectors;

public class StreamExample {
    public static void main(String[] args) {
        List<String> nomes = List.of("Ana", "Bruno", "Beatriz", "Carlos", "Amanda");

        // filtrar nomes que começam com 'A', transformar em maiúsculas e juntar em string
        String resultado = nomes.stream()
                .filter(n -> n.startsWith("A"))
                .map(String::toUpperCase)
                .collect(Collectors.joining(", "));

        System.out.println("Nomes que começam com A: " + resultado);
    }
}
