# Insecure Design 

Um **Design Seguro** consiste em uma metodologia e uma cultura que recomenda **projetar o código, testá-lo e implementá-lo de uma forma segura**, dessa forma, logo no início os riscos são mapeados e mitigados. Vulnerabilidades que apresentam lógica de negócio, fluxos de dados, controle de acessos, propensões a falhas de seguranças no geral, todas são corrigidas antes do sistema entrar em produção, o que garante uma maior maturidade de segurança, menos retrabalho,  e menos gastos para a empresa.

Uma vulnerabilidade classificada como **Design Inseguro** pode surgir de vários pontos, e mesmo com uma implementação bem sucedida, essas vulnerabilidades são bem difíceis de serem corrigidas, uma vez que não foram criados os controles necessários logo no início. Projetos legados geralmente são cheio delas e permanecem até quando o mesmo for descontinuado. 

### SSDL 

Quando falando de Secure Software Development Lifecicle, podemos considerar o uso de Design Seguro e projetar os sistemas de forma que sejam criados com o máximo se segurança possível, aqui vale padrões que sejam aplicados nos demais projetos, componentes, libraries, ferramentas, análises de código, testes, e modelagem de ameaça. 

A consultoria do time de segurança e sempre bem-vinda pra fornecer suporte nesse planejamento e o processo de manutenção, existem no mercado vários frameworks que podem ajudar nessa etapa: OWASP SAMM, CWE, NIST... 

### Exemplos:
1. CWE-259 - **Uso de Senha Hardcoded**

O software contém senhas dentro do código em texto plano. Todas as pessoas que tiverem acesso a esse código também terão acesso a senha e, em caso de vazamento de dados, permite ao atacante acessar o sistema correspondente.  

Uma vez que esse problema é detectado, a sua correção pode ser mais complicada por poder desabilitar uma aplicação e/ou um serviço. 

<code> connectionStrings </code>

<code> add name="ud_DEV" connectionString="connectDB=uDB; uid=db2admin; pwd=password; dbalias=uDB;" providerName="System.Data.Odbc"  </code>

<code> /connectionStrings </code>


### Formas de Prevenção: 

- Estabeleça e use um ciclo de vida de desenvolvimento seguro com profissionais da AppSec para ajudar a avaliar e projetar controles relacionados à segurança e privacidade
- Estabeleça e use uma biblioteca de padrões de projeto seguros ou componentes prontos 
- Use a modelagem de ameaças para autenticações, controle de acesso, lógica de negócios e fluxos existentes 
- Escreva testes de unidade e integração para validar se todos os fluxos críticos são resistentes ao modelo de ameaça. Levante os casos de uso válidos e casos de uso indevido para cada camada da sua aplicação 
- Segregar camadas sistema e rede, dependendo das necessidades de exposição e proteção de cada aplicação 
- Uso de ferramentas para análise de código estático e dinâmico (SAST e DAST) 
- Monitoramento das aplicações 
- Testes de carga e estresse 


### Referências: 
- OWASP Cheat Sheet: Secure Design Principles
- OWASP SAMM: Design:Security Architecture
- OWASP SAMM: Design:Threat Assessment
- NIST – Guidelines on Minimum Standards for Developer Verification of Software
- The Threat Modeling Manifesto
- Awesome Threat Modeling
- CWE-183 Permissive List of Allowed Inputs
- CWE-209 Generation of Error Message Containing Sensitive Information
- CWE-213 Exposure of Sensitive Information Due to Incompatible Policies
- CWE-256 Unprotected Storage of Credentials
- CWE-257 Storing Passwords in a Recoverable Format
