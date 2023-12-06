const alunos = [
  {
    nome: "João",
    notas: [8, 7, 9],
    endereco: { rua: "Rua A", cidade: "Cidade X" }
  },
  {
    nome: "Maria",
    notas: [6, 5, 7],
    endereco: { rua: "Rua B", cidade: "Cidade Y" }
  },
  {
    nome: "Pedro",
    notas: [7, 8, 6],
    endereco: { rua: "Rua C", cidade: "Cidade Z" }
  }
];

const calcularMedia = notas => notas.reduce((acc, nota) => acc + nota, 0) / notas.length;


alunos.forEach(aluno => {
  const media = calcularMedia(aluno.notas);
  const status = media >= 7 ? "aprovado(a)" : "reprovado(a)";

  console.log(`Aluno(a) ${aluno.nome} com notas ${aluno.notas.join(", ")} mora em ${aluno.endereco.rua}, ${aluno.endereco.cidade} e teve a média ${media.toFixed(2)}, portanto foi ${status}.`);
});