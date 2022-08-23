# CODIFICA-O---Entro-Remoto-1
Classe 
public abstract class Pessoa : IPessoa
    {
        public string? nome { get; set;}
        public float rendimento{ get; set; }

        public string? endereco { get; set; }
        public abstract float CalcularImposto (float rendimento);
        
        public class PessoaFisica : Pessoa, IPessoafisica 
    {
        public DateTime dataNasc { get; set; }
        public string? cpf  { get; set; }

        public override float CalcularImposto(float rendimento)
        {
            throw new NotImplementedException();
        }

        public override bool Equals(object? obj)
        {
            return base.Equals(obj);
        }

        public override int GetHashCode()
        {
            return base.GetHashCode();
        }

        public override string? ToString()
        {
            return base.ToString();
        }

        public bool ValidarDataNasc(DateTime datanasc)
        {
            throw new NotImplementedException();
        }
    }
    
    
    public class PessoaJuridica : IPessoaJuridica
    {
        public string? razãosocial { get; set; }
        public string? cnpj { get; set; }
        public bool ValidarCnpj(string cnpj)
        {
            throw new NotImplementedException();
            
            Interfaces
            public interface IPessoa
    {
        float CalcularImposto(float rendimento);
        
        
    public interface IPessoajuridica
    {
       bool Validarcnpj(string cnpj);
