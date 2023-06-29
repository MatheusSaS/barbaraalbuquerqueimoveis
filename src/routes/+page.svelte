<script>

  let nome = "";
  let email = "";
  let telefone = "";
  let bairro = "";
  let mensagem = ''
  let selectedOption = 'De 150 a 200 metros';

  function onSubmit() {
    if (nome == "" || nome == undefined) {
      alert("Preencha o nome corretamente");
      return;
    }
    if (email == "" || email == undefined) {
      alert("Preencha o email corretamente");
      return;
    }
    if (telefone == "" || telefone == undefined) {
      alert("Preencha o telefone corretamente");
      return;
    }
    if (bairro == "" || bairro == undefined) {
      alert("Preencha o bairro corretamente");
      return;
    }
    mensagem = `
          Olá Bárbara, vim através do seu formulário.%0A
          %0A•Nome%3A ${nome} %0A
          %0A•Email%3A ${email} %0A
          %0A•Telefone%3A ${telefone} %0A
          %0A•Bairro%3A ${bairro} %0A
          %0A•Metragem%3A ${selectedOption} %0A
          `;
    window.open(`
        https://api.whatsapp.com/send/?phone=5511991694514&text=${mensagem}
      `);
  }
</script>

<main class="mt-0 transition-all duration-200 ease-soft-in-out bg-black">
  <section class="mb-20">
    <div
      id="img"
      class="relative flex items-start overflow-hidden doodles-light bg-cover min-h-50-screen bg-[url('/fundo.jpg')]"
    >
      <span
        class="absolute top-0 left-0 w-full h-full bg-center bg-cover opacity-60 bg-gradient-to-tl from-black to-gray-900"
      />
      <div class="w-full z-1">
        <div class="flex flex-wrap justify-center">
          <img src="/logo.png" alt="logo" class="relative w-80" />
        </div>
      </div>
    </div>
    <div
      class="absolute bottom-0 left-0 right-0 h-32 bg-black transform -skew-y-2 top-80 border-t-8 border-[#b89748]"
    />
    <div class="flex justify-center">
      <div class="container m-6">
        <div class="flex flex-wrap">
          <div
            class="w-full max-w-full px-3 mx-auto mt-0 md:flex-0 shrink-0 lg:w-1/2"
          >
            <div
              class="relative z-0 text-center flex flex-col min-w-0 break-words bg-dark border-0 shadow-md rounded-lg border-base-200"
            >
              <p class="text-gray-300 mb-8">
                Preencha o formulário e entraremos em contato com o seu imóvel de
                Alto Padrão
              </p>
              <div class="flex-auto p-6">
                <div class="flex items-center border rounded-lg mb-3">
                  <input
                    class="py-4 pl-4 w-full placeholder-gray-400 focus:outline-none border-0 focus:border border-base-300 focus:border-[#b89748] rounded-lg bg-[#202020]"
                    id="Nome"
                    name="Nome"
                    placeholder="Nome"
                    bind:value={nome}
                  />
                </div>
                <div class="flex items-center border rounded-lg mb-3">
                  <input
                    class="py-4 pl-4 w-full placeholder-gray-400 focus:outline-none border-0 focus:border border-base-300 focus:border-[#b89748] rounded-lg bg-[#202020]"
                    id="email"
                    name="email"
                    placeholder="E-mail"
                    bind:value={email}
                  />
                </div>
                <div class="flex items-center border rounded-lg mb-3">
                  <input
                    class="py-4 pl-4 w-full placeholder-gray-400 focus:outline-none border-0 focus:border border-base-300 focus:border-[#b89748] rounded-lg bg-[#202020]"
                    id="Telefone"
                    name="Telefone"
                    placeholder="Telefone"
                    bind:value={telefone}
                  />
                </div>
                <div class="flex items-center border rounded-lg mb-3">
                  <input
                    class="py-4 pl-4 w-full placeholder-gray-400 focus:outline-none border-0 focus:border border-base-300 focus:border-[#b89748] rounded-lg bg-[#202020]"
                    id="bairro"
                    name="bairro"
                    placeholder="Bairro"
                    bind:value={bairro}
                  />
                </div>
                Metragem:
                <div class="flex items-center border rounded-lg mb-3">
                  <div class="py-4 pl-4 w-full placeholder-gray-400 focus:outline-none border-0 focus:border border-base-300 focus:border-[#b89748] rounded-lg bg-[#202020]">
                    <div class="form-control">
                      <label class="label cursor-pointer">
                        <span class="label-text">De 150 a 200 metros</span>
                        <input type="radio" name="radio-10" class="radio" value="De 150 a 200 metros" bind:group={selectedOption} />
                      </label>
                    </div>
                    <div class="form-control">
                      <label class="label cursor-pointer">
                        <span class="label-text">De 200 a 250 metros</span>
                        <input type="radio" name="radio-10" class="radio" value="De 200 a 250 metros" bind:group={selectedOption} />
                      </label>
                    </div>
                    <div class="form-control">
                      <label class="label cursor-pointer">
                        <span class="label-text">Acima de 250 metros</span>
                        <input type="radio" name="radio-10" class="radio" value="Acima de 250 metros" bind:group={selectedOption} />
                      </label>
                    </div>
                  </div>
                </div>
                <div class="text-center mt-6">
                  <button
                   on:click={() => onSubmit()}
                    class="group relative h-12 w-48 overflow-hidden rounded-2xl bg-[#b89748] text-lg font-bold text-white"
                  >
                    ENVIAR
                    <div
                      class="absolute inset-0 h-full w-full scale-0 rounded-2xl transition-all duration-300 group-hover:scale-100 group-hover:bg-white/30"
                    />
                  </button>
                </div>
              </div>
              <p class="text-gray-300 mt-8 text-xs">
                A sua privacidade e a segurança dos seus dados são de extrema
                importância para nós. Por isso, queremos garantir que adotamos
                todas as medidas necessárias para proteger as suas informações.
              </p>

              <p class="text-gray-300 mt-8">
                <span class="text-[#b89748]">Bárbara Albuquerque Imóveis</span>
                | Todos os direitos reservados
                <span class="text-[#b89748]">@2023</span>
              </p>
            </div>
          </div>
        </div>
      </div>
      <!--<PnlLogin>-->
    </div>
  </section>
</main>
