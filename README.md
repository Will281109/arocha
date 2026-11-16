[Uploading index.html…]()
<!DOCTYPE html>
<html lang="pt-BR" class="scroll-smooth">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>A Rocha Gestão e Serviços | Manutenção, Reformas & Zeladoria no Paraguai</title>
  <!-- Tailwind CSS -->
  <script src="https://cdn.tailwindcss.com"></script>
  <!-- Google Fonts: Inter & Plus Jakarta Sans -->
  <link rel="preconnect" href="https://fonts.googleapis.com" />
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin />
  <link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;500;600;700&family=Plus+Jakarta+Sans:wght@700;800&display=swap" rel="stylesheet" />
  <!-- Font Awesome Icons -->
  <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.5.1/css/all.min.css" />

  <script>
    tailwind.config = {
      theme: {
        extend: {
          fontFamily: {
            sans: ['Inter', 'sans-serif'],
            display: ['Plus Jakarta Sans', 'sans-serif'],
          },
          colors: {
            brand: {
              dark: '#06241B',
              forest: '#0C3B2E',
              emerald: '#15803D',
              accent: '#D97706',
              gold: '#FBBF24',
            }
          }
        }
      }
    };
  </script>
  <style>
    .solid-nav {
      background: #06241B;
    }
    .card-hover {
      transition: all 0.25s cubic-bezier(0.4, 0, 0.2, 1);
    }
    .card-hover:hover {
      transform: translateY(-5px);
      box-shadow: 0 20px 25px -5px rgba(15, 23, 42, 0.12), 0 8px 10px -6px rgba(15, 23, 42, 0.08);
    }
  </style>
</head>
<body class="bg-slate-50 text-slate-900 antialiased selection:bg-amber-400 selection:text-slate-950">

  <!-- ==================== TOP NAVIGATION ==================== -->
  <header class="fixed top-0 inset-x-0 z-50 solid-nav border-b border-emerald-900/80 text-white shadow-md">
    <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
      <div class="flex items-center justify-between h-20">
        <!-- Brand Logo -->
        <a href="#inicio" class="flex items-center gap-3 group">
          <div class="w-11 h-11 rounded-xl bg-amber-400 flex items-center justify-center text-slate-950 font-extrabold text-xl shadow-md group-hover:scale-105 transition">
            <i class="fa-solid fa-mountain-sun"></i>
          </div>
          <div>
            <span class="font-display font-extrabold text-lg sm:text-xl tracking-tight text-white block leading-none">
              A ROCHA
            </span>
            <span class="text-[11px] uppercase tracking-[0.18em] text-amber-300 font-bold block mt-1" data-i18n="brand_sub">
              Gestão e Serviços
            </span>
          </div>
        </a>

        <!-- Desktop Links -->
        <nav class="hidden lg:flex items-center gap-7 text-sm font-semibold text-white">
          <a href="#vantagens" class="hover:text-amber-300 transition" data-i18n="nav_why">Diferenciais</a>
          <a href="#servicos" class="hover:text-amber-300 transition" data-i18n="nav_services">Nossos Serviços</a>
          <a href="#planos" class="hover:text-amber-300 transition" data-i18n="nav_plans">Planos & Preços</a>
          <a href="#como-funciona" class="hover:text-amber-300 transition" data-i18n="nav_how">Como Funciona</a>
          <a href="#orcamento" class="hover:text-amber-300 transition" data-i18n="nav_contact">Orçamento</a>
        </nav>

        <!-- Controls: Language Switcher & WhatsApp CTA -->
        <div class="flex items-center gap-3">
          <!-- PT / ES Switcher -->
          <div class="flex items-center bg-emerald-950 rounded-xl p-1 border border-emerald-700/70">
            <button onclick="setLanguage('pt')" id="btn-pt" class="px-2.5 py-1.5 rounded-lg text-xs font-extrabold transition bg-amber-400 text-slate-950">
              🇧🇷 PT
            </button>
            <button onclick="setLanguage('es')" id="btn-es" class="px-2.5 py-1.5 rounded-lg text-xs font-extrabold transition text-white hover:text-amber-300">
              🇵🇾 ES
            </button>
          </div>

          <a href="#orcamento" class="hidden sm:inline-flex items-center gap-2 bg-emerald-600 hover:bg-emerald-500 text-white text-sm font-bold px-4 py-2.5 rounded-xl shadow transition">
            <i class="fa-brands fa-whatsapp text-base"></i>
            <span data-i18n="nav_cta">Solicitar Orçamento</span>
          </a>

          <!-- Mobile Hamburger -->
          <button id="mobile-menu-btn" class="lg:hidden p-2.5 rounded-xl bg-emerald-900 hover:bg-emerald-800 text-white" aria-label="Menu">
            <i class="fa-solid fa-bars text-lg"></i>
          </button>
        </div>
      </div>
    </div>

    <!-- Mobile Dropdown Menu -->
    <div id="mobile-menu" class="hidden lg:hidden bg-brand-dark border-t border-emerald-800 px-4 pt-3 pb-6 space-y-2 text-white">
      <a href="#vantagens" onclick="closeMobileMenu()" class="block px-3 py-2.5 rounded-xl hover:bg-emerald-900 text-sm font-semibold" data-i18n="nav_why">Diferenciais</a>
      <a href="#servicos" onclick="closeMobileMenu()" class="block px-3 py-2.5 rounded-xl hover:bg-emerald-900 text-sm font-semibold" data-i18n="nav_services">Nossos Serviços</a>
      <a href="#planos" onclick="closeMobileMenu()" class="block px-3 py-2.5 rounded-xl hover:bg-emerald-900 text-sm font-semibold" data-i18n="nav_plans">Planos & Preços</a>
      <a href="#como-funciona" onclick="closeMobileMenu()" class="block px-3 py-2.5 rounded-xl hover:bg-emerald-900 text-sm font-semibold" data-i18n="nav_how">Como Funciona</a>
      <a href="#orcamento" onclick="closeMobileMenu()" class="block mt-3 text-center bg-amber-400 text-slate-950 font-extrabold py-3 rounded-xl text-sm" data-i18n="nav_cta">Solicitar Orçamento</a>
    </div>
  </header>

  <!-- ==================== HERO SECTION (CLEAN SPLIT LAYOUT - ZERO TEXT OVERLAP) ==================== -->
  <section id="inicio" class="bg-brand-dark pt-28 pb-16 lg:pt-32 lg:pb-24 border-b border-emerald-900">
    <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
      <div class="grid lg:grid-cols-12 gap-10 lg:gap-12 items-center">
        
        <!-- Left Content: Solid Dark Emerald Canvas for 100% Sharp Text Legibility -->
        <div class="lg:col-span-6 text-white space-y-6">
          <div class="inline-flex items-center gap-2.5 bg-emerald-900/90 border border-emerald-600/60 px-4 py-2 rounded-full text-xs sm:text-sm font-bold text-amber-300">
            <span class="w-2.5 h-2.5 rounded-full bg-emerald-400"></span>
            <span data-i18n="hero_badge">Hugua Hú • Atyrá • Altos • Caacupé • San Bernardino</span>
          </div>

          <h1 class="font-display font-extrabold text-3xl sm:text-5xl lg:text-[50px] text-white leading-[1.14] tracking-tight" data-i18n="hero_title">
            Sua Casa ou Quinta Sempre Impecável. <span class="text-amber-300">Tudo em Um Só Lugar.</span>
          </h1>

          <p class="text-base sm:text-lg text-slate-100 leading-relaxed font-normal" data-i18n="hero_subtitle">
            Na <strong class="text-white font-bold">A Rocha Gestão e Serviços</strong>, cuidamos de reformas rápidas ("Marido de Aluguel"), limpeza pós-obra, jardinagem, manutenção de piscinas e zeladoria semanal com <strong class="text-amber-300 font-semibold">relatórios por foto no WhatsApp</strong> e <strong class="text-white font-semibold">Factura Legal</strong>.
          </p>

          <!-- CTAs -->
          <div class="flex flex-col sm:flex-row gap-4 pt-2">
            <a href="#planos" class="inline-flex items-center justify-center gap-2.5 bg-amber-400 hover:bg-amber-300 text-slate-950 font-extrabold px-7 py-4 rounded-2xl shadow-lg transition text-base">
              <i class="fa-solid fa-layer-group"></i>
              <span data-i18n="hero_btn_plans">Ver 5 Planos e Preços</span>
            </a>
            <a href="#orcamento" class="inline-flex items-center justify-center gap-2.5 bg-emerald-700 hover:bg-emerald-600 border border-emerald-500 text-white font-bold px-7 py-4 rounded-2xl transition text-base">
              <i class="fa-brands fa-whatsapp text-xl"></i>
              <span data-i18n="hero_btn_quote">Orçamento Rápido</span>
            </a>
          </div>

          <!-- Trust Metrics -->
          <div class="grid grid-cols-3 gap-4 pt-6 border-t border-emerald-800">
            <div>
              <p class="font-display font-extrabold text-xl sm:text-2xl text-amber-300" data-i18n="stat_1_v">Gestão Total</p>
              <p class="text-xs sm:text-sm text-slate-200 font-medium mt-0.5" data-i18n="stat_1">Manutenção e obras</p>
            </div>
            <div>
              <p class="font-display font-extrabold text-xl sm:text-2xl text-emerald-300" data-i18n="stat_2_v">100% Visual</p>
              <p class="text-xs sm:text-sm text-slate-200 font-medium mt-0.5" data-i18n="stat_2">Relatório com fotos</p>
            </div>
            <div>
              <p class="font-display font-extrabold text-xl sm:text-2xl text-white" data-i18n="stat_3_v">Factura Legal</p>
              <p class="text-xs sm:text-sm text-slate-200 font-medium mt-0.5" data-i18n="stat_3">Empresa formalizada</p>
            </div>
          </div>
        </div>

        <!-- Right Visual Showcase: Clean Framed Photo Card (No cluttered text over photo) -->
        <div class="lg:col-span-6">
          <div class="bg-white rounded-3xl p-3 sm:p-4 shadow-2xl border border-emerald-800/40">
            <div class="relative rounded-2xl overflow-hidden h-64 sm:h-80 lg:h-[360px]">
              <img
                src="https://images.unsplash.com/photo-1613490493576-7fde63acd811?auto=format&fit=crop&w=1200&q=85"
                onerror="this.src='https://placehold.co/1200x800/0C3B2E/FFFFFF?text=A+Rocha+Gestao+e+Servicos'"
                alt="Casa de campo moderna com piscina cristalina e jardim cuidado"
                class="w-full h-full object-cover object-center"
              />
            </div>

            <!-- Clean White Status Bar Below Photo (100% Legible) -->
            <div class="pt-4 pb-2 px-2 flex flex-col sm:flex-row sm:items-center justify-between gap-3">
              <div class="flex items-center gap-3">
                <div class="w-10 h-10 rounded-xl bg-emerald-100 text-emerald-800 flex items-center justify-center text-lg shrink-0">
                  <i class="fa-solid fa-camera-retro"></i>
                </div>
                <div>
                  <p class="font-display font-extrabold text-sm text-slate-900" data-i18n="card_report_title">Relatório Semanal de Quinta</p>
                  <p class="text-xs font-medium text-slate-700" data-i18n="card_report_sub">Piscina tratada, grama cortada e casa ventilada</p>
                </div>
              </div>
              <span class="inline-flex items-center gap-1.5 bg-emerald-700 text-white text-xs font-bold px-3.5 py-1.5 rounded-full self-start sm:self-center">
                <i class="fa-solid fa-check"></i>
                <span data-i18n="card_status">Pronta para o Fim de Semana</span>
              </span>
            </div>
          </div>
        </div>

      </div>
    </div>
  </section>

  <!-- ==================== WHY CHOOSE US (VANTAGENS) ==================== -->
  <section id="vantagens" class="py-20 bg-white">
    <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
      <div class="text-center max-w-3xl mx-auto mb-14">
        <span class="inline-block bg-amber-100 text-amber-900 font-extrabold text-xs uppercase tracking-widest px-3.5 py-1.5 rounded-full" data-i18n="why_kicker">
          Por que contratar a A Rocha?
        </span>
        <h2 class="font-display font-extrabold text-3xl sm:text-4xl text-slate-950 mt-3" data-i18n="why_title">
          Acabamos com a dor de cabeça de gerenciar vários prestadores
        </h2>
        <p class="text-slate-700 mt-3 text-base sm:text-lg leading-relaxed" data-i18n="why_desc">
          Sabemos como é difícil encontrar mão de obra pontual e confiável no interior. Criamos uma gestão profissional com padrão empresarial para cuidar do seu patrimônio.
        </p>
      </div>

      <div class="grid sm:grid-cols-2 lg:grid-cols-4 gap-6">
        <!-- Advantage 1 -->
        <div class="bg-slate-50 border border-slate-200 rounded-3xl p-7 card-hover">
          <div class="w-14 h-14 rounded-2xl bg-emerald-700 text-white flex items-center justify-center text-2xl mb-5 shadow-sm">
            <i class="fa-solid fa-clock-rotate-left"></i>
          </div>
          <h3 class="font-display font-extrabold text-lg text-slate-950 mb-2" data-i18n="adv_1_t">Pontualidade & Compromisso</h3>
          <p class="text-slate-700 text-sm leading-relaxed" data-i18n="adv_1_d">
            Cronograma rígido de visitas e prazos de entrega cumpridos à risca. Sem sumiços no meio da obra ou desculpas.
          </p>
        </div>

        <!-- Advantage 2 -->
        <div class="bg-slate-50 border border-slate-200 rounded-3xl p-7 card-hover">
          <div class="w-14 h-14 rounded-2xl bg-amber-500 text-slate-950 flex items-center justify-center text-2xl mb-5 shadow-sm">
            <i class="fa-brands fa-whatsapp"></i>
          </div>
          <h3 class="font-display font-extrabold text-lg text-slate-950 mb-2" data-i18n="adv_2_t">Relatórios Visuais no WhatsApp</h3>
          <p class="text-slate-700 text-sm leading-relaxed" data-i18n="adv_2_d">
            Mora em Assunção ou no Brasil? Receba fotos do antes e depois a cada visita semanal da nossa equipe na sua quinta.
          </p>
        </div>

        <!-- Advantage 3 -->
        <div class="bg-slate-50 border border-slate-200 rounded-3xl p-7 card-hover">
          <div class="w-14 h-14 rounded-2xl bg-slate-900 text-amber-300 flex items-center justify-center text-2xl mb-5 shadow-sm">
            <i class="fa-solid fa-toolbox"></i>
          </div>
          <h3 class="font-display font-extrabold text-lg text-slate-950 mb-2" data-i18n="adv_3_t">1 Único Contato Resolve Tudo</h3>
          <p class="text-slate-700 text-sm leading-relaxed" data-i18n="adv_3_d">
            Do corte de grama e limpeza da piscina até pintura, elétrica, ar-condicionado e limpeza pós-obra sob uma única gestão.
          </p>
        </div>

        <!-- Advantage 4 -->
        <div class="bg-slate-50 border border-slate-200 rounded-3xl p-7 card-hover">
          <div class="w-14 h-14 rounded-2xl bg-emerald-700 text-white flex items-center justify-center text-2xl mb-5 shadow-sm">
            <i class="fa-solid fa-file-invoice-dollar"></i>
          </div>
          <h3 class="font-display font-extrabold text-lg text-slate-950 mb-2" data-i18n="adv_4_t">Garantia & Factura Legal</h3>
          <p class="text-slate-700 text-sm leading-relaxed" data-i18n="adv_4_d">
            Empresa formalizada no Paraguai, equipe uniformizada, supervisão técnica e emissão de Factura para sua segurança.
          </p>
        </div>
      </div>
    </div>
  </section>

  <!-- ==================== ORGANIC SERVICE PORTFOLIO ==================== -->
  <section id="servicos" class="py-20 bg-slate-100 border-y border-slate-200">
    <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
      <div class="flex flex-col md:flex-row md:items-end justify-between mb-14 gap-6">
        <div class="max-w-2xl">
          <span class="inline-block bg-emerald-100 text-emerald-900 font-extrabold text-xs uppercase tracking-widest px-3.5 py-1.5 rounded-full" data-i18n="srv_kicker">
            Soluções Completas para Casas e Quintas
          </span>
          <h2 class="font-display font-extrabold text-3xl sm:text-4xl text-slate-950 mt-3" data-i18n="srv_title">
            Tudo o que Sua Propriedade Precisa em Um Só Lugar
          </h2>
          <p class="text-slate-700 mt-3 text-base leading-relaxed" data-i18n="srv_desc">
            Contamos com equipe própria polivalente e especialistas técnicos credenciados para cada tipo de demanda na sua residência ou chácara.
          </p>
        </div>
        <a href="#orcamento" class="inline-flex items-center gap-2 bg-slate-900 hover:bg-slate-800 text-white font-bold px-5 py-3 rounded-xl text-sm transition shrink-0">
          <span data-i18n="srv_link">Solicitar serviço avulso</span>
          <i class="fa-solid fa-arrow-right"></i>
        </a>
      </div>

      <div class="grid md:grid-cols-2 lg:grid-cols-3 gap-8">
        <!-- Service 1: Reformas -->
        <div class="bg-white rounded-3xl overflow-hidden shadow-sm border border-slate-200 card-hover flex flex-col">
          <div class="relative h-52 overflow-hidden bg-slate-200">
            <img src="https://images.unsplash.com/photo-1581578731548-c64695cc6952?auto=format&fit=crop&w=800&q=80"
                 onerror="this.src='https://placehold.co/800x500/06241B/FFFFFF?text=Reformas+e+Manutencao'"
                 alt="Reformas simples e pintura" class="w-full h-full object-cover" />
            <span class="absolute top-3.5 left-3.5 bg-slate-950 text-amber-300 text-xs font-extrabold px-3.5 py-1.5 rounded-full shadow" data-i18n="s1_badge">
              Mais Procurado
            </span>
          </div>
          <div class="p-6 flex-1 flex flex-col">
            <h3 class="font-display font-extrabold text-xl text-slate-950 mb-3" data-i18n="s1_t">Reformas Simples & Marido de Aluguel</h3>
            <ul class="space-y-2.5 text-sm text-slate-800 flex-1">
              <li class="flex items-start gap-2.5"><i class="fa-solid fa-circle-check text-emerald-700 mt-1"></i><span data-i18n="s1_l1">Pintura residencial e comercial (interna e externa)</span></li>
              <li class="flex items-start gap-2.5"><i class="fa-solid fa-circle-check text-emerald-700 mt-1"></i><span data-i18n="s1_l2">Reparos de alvenaria, reboco, pisos e rejuntamento</span></li>
              <li class="flex items-start gap-2.5"><i class="fa-solid fa-circle-check text-emerald-700 mt-1"></i><span data-i18n="s1_l3">Instalação de drywall, forros e divisórias</span></li>
              <li class="flex items-start gap-2.5"><i class="fa-solid fa-circle-check text-emerald-700 mt-1"></i><span data-i18n="s1_l4">Elétrica e hidráulica básica (torneiras, chuveiros, tomadas, luminárias)</span></li>
              <li class="flex items-start gap-2.5"><i class="fa-solid fa-circle-check text-emerald-700 mt-1"></i><span data-i18n="s1_l5">Montagem de móveis, cortinas, suportes de TV e prateleiras</span></li>
            </ul>
          </div>
        </div>

        <!-- Service 2: Limpeza -->
        <div class="bg-white rounded-3xl overflow-hidden shadow-sm border border-slate-200 card-hover flex flex-col">
          <div class="relative h-52 overflow-hidden bg-slate-200">
            <img src="https://images.unsplash.com/photo-1527515637462-cff94eecc1ac?auto=format&fit=crop&w=800&q=80"
                 onerror="this.src='https://placehold.co/800x500/06241B/FFFFFF?text=Limpeza+Pos-Obra'"
                 alt="Limpeza pós-obra especializada" class="w-full h-full object-cover" />
            <span class="absolute top-3.5 left-3.5 bg-emerald-800 text-white text-xs font-extrabold px-3.5 py-1.5 rounded-full shadow" data-i18n="s2_badge">
              Alta Precisão
            </span>
          </div>
          <div class="p-6 flex-1 flex flex-col">
            <h3 class="font-display font-extrabold text-xl text-slate-950 mb-3" data-i18n="s2_t">Limpeza Especializada & Pós-Obra</h3>
            <ul class="space-y-2.5 text-sm text-slate-800 flex-1">
              <li class="flex items-start gap-2.5"><i class="fa-solid fa-circle-check text-emerald-700 mt-1"></i><span data-i18n="s2_l1"><strong>Limpeza Pós-Obra Fina:</strong> Remoção técnica de tinta, cimento e poeira sem riscar porcelanatos</span></li>
              <li class="flex items-start gap-2.5"><i class="fa-solid fa-circle-check text-emerald-700 mt-1"></i><span data-i18n="s2_l2">Faxina pesada pré e pós-mudança</span></li>
              <li class="flex items-start gap-2.5"><i class="fa-solid fa-circle-check text-emerald-700 mt-1"></i><span data-i18n="s2_l3">Hidrolavagem de telhados coloniais, muros de pedra, decks e calçadas</span></li>
            </ul>
          </div>
        </div>

        <!-- Service 3: Jardinagem -->
        <div class="bg-white rounded-3xl overflow-hidden shadow-sm border border-slate-200 card-hover flex flex-col">
          <div class="relative h-52 overflow-hidden bg-slate-200">
            <img src="https://images.unsplash.com/photo-1558904541-efa843a96f01?auto=format&fit=crop&w=800&q=80"
                 onerror="this.src='https://placehold.co/800x500/06241B/FFFFFF?text=Jardinagem+e+Paisagismo'"
                 alt="Jardinagem e corte de grama em jardim residencial" class="w-full h-full object-cover" />
            <span class="absolute top-3.5 left-3.5 bg-emerald-800 text-white text-xs font-extrabold px-3.5 py-1.5 rounded-full shadow" data-i18n="s3_badge">
              Áreas Verdes
            </span>
          </div>
          <div class="p-6 flex-1 flex flex-col">
            <h3 class="font-display font-extrabold text-xl text-slate-950 mb-3" data-i18n="s3_t">Jardinagem & Áreas Externas</h3>
            <ul class="space-y-2.5 text-sm text-slate-800 flex-1">
              <li class="flex items-start gap-2.5"><i class="fa-solid fa-circle-check text-emerald-700 mt-1"></i><span data-i18n="s3_l1">Corte de grama, acabamento de bordas e poda de árvores/arbustos</span></li>
              <li class="flex items-start gap-2.5"><i class="fa-solid fa-circle-check text-emerald-700 mt-1"></i><span data-i18n="s3_l2">Roçada pesada e limpeza de terrenos e lotes fechados</span></li>
              <li class="flex items-start gap-2.5"><i class="fa-solid fa-circle-check text-emerald-700 mt-1"></i><span data-i18n="s3_l3">Adubação e controle preventivo de pragas (formigas <em>ysaú</em> e cupins)</span></li>
            </ul>
          </div>
        </div>

        <!-- Service 4: Piscinas -->
        <div class="bg-white rounded-3xl overflow-hidden shadow-sm border border-slate-200 card-hover flex flex-col">
          <div class="relative h-52 overflow-hidden bg-slate-200">
            <img src="https://images.unsplash.com/photo-1572331165267-854da2b10ccc?auto=format&fit=crop&w=800&q=80"
                 onerror="this.src='https://placehold.co/800x500/06241B/FFFFFF?text=Manutencao+de+Piscinas'"
                 alt="Manutenção de piscina cristalina" class="w-full h-full object-cover" />
            <span class="absolute top-3.5 left-3.5 bg-sky-900 text-white text-xs font-extrabold px-3.5 py-1.5 rounded-full shadow" data-i18n="s4_badge">
              Água Cristalina
            </span>
          </div>
          <div class="p-6 flex-1 flex flex-col">
            <h3 class="font-display font-extrabold text-xl text-slate-950 mb-3" data-i18n="s4_t">Manutenção Completa de Piscinas</h3>
            <ul class="space-y-2.5 text-sm text-slate-800 flex-1">
              <li class="flex items-start gap-2.5"><i class="fa-solid fa-circle-check text-emerald-700 mt-1"></i><span data-i18n="s4_l1">Aspiração, peneiramento e escovação semanal de bordas</span></li>
              <li class="flex items-start gap-2.5"><i class="fa-solid fa-circle-check text-emerald-700 mt-1"></i><span data-i18n="s4_l2">Controle químico rigoroso (pH, cloro, alcalinidade e algicida)</span></li>
              <li class="flex items-start gap-2.5"><i class="fa-solid fa-circle-check text-emerald-700 mt-1"></i><span data-i18n="s4_l3">Manutenção preventiva de bomba, filtro e casa de máquinas</span></li>
            </ul>
          </div>
        </div>

        <!-- Service 5: Zeladoria -->
        <div class="bg-white rounded-3xl overflow-hidden shadow-sm border border-slate-200 card-hover flex flex-col">
          <div class="relative h-52 overflow-hidden bg-slate-200">
            <img src="https://images.unsplash.com/photo-1512917774080-9991f1c4c750?auto=format&fit=crop&w=800&q=80"
                 onerror="this.src='https://placehold.co/800x500/06241B/FFFFFF?text=Zeladoria+e+Casa+Pronta'"
                 alt="Zeladoria e casa de campo pronta" class="w-full h-full object-cover" />
            <span class="absolute top-3.5 left-3.5 bg-amber-400 text-slate-950 text-xs font-extrabold px-3.5 py-1.5 rounded-full shadow" data-i18n="s5_badge">
              Exclusivo Quintas
            </span>
          </div>
          <div class="p-6 flex-1 flex flex-col">
            <h3 class="font-display font-extrabold text-xl text-slate-950 mb-3" data-i18n="s5_t">Zeladoria & "Casa Pronta"</h3>
            <ul class="space-y-2.5 text-sm text-slate-800 flex-1">
              <li class="flex items-start gap-2.5"><i class="fa-solid fa-circle-check text-emerald-700 mt-1"></i><span data-i18n="s5_l1">Vistoria semanal, abertura para ventilação e checagem pós-chuva</span></li>
              <li class="flex items-start gap-2.5"><i class="fa-solid fa-circle-check text-emerald-700 mt-1"></i><span data-i18n="s5_l2"><strong>Preparação Pré-Chegada:</strong> Ligamos geladeira, ar-condicionado e luzes antes da sua família chegar na sexta-feira</span></li>
              <li class="flex items-start gap-2.5"><i class="fa-solid fa-circle-check text-emerald-700 mt-1"></i><span data-i18n="s5_l3">Relatório semanal com fotos enviado no WhatsApp</span></li>
            </ul>
          </div>
        </div>

        <!-- Service 6: Instalações Técnicas -->
        <div class="bg-white rounded-3xl overflow-hidden shadow-sm border border-slate-200 card-hover flex flex-col">
          <div class="relative h-52 overflow-hidden bg-slate-200">
            <img src="https://images.unsplash.com/photo-1558002038-1055907df827?auto=format&fit=crop&w=800&q=80"
                 onerror="this.src='https://placehold.co/800x500/06241B/FFFFFF?text=Instalacoes+Tecnicas'"
                 alt="Instalações técnicas e segurança" class="w-full h-full object-cover" />
            <span class="absolute top-3.5 left-3.5 bg-slate-950 text-amber-300 text-xs font-extrabold px-3.5 py-1.5 rounded-full shadow" data-i18n="s6_badge">
              Conforto & Técnica
            </span>
          </div>
          <div class="p-6 flex-1 flex flex-col">
            <h3 class="font-display font-extrabold text-xl text-slate-950 mb-3" data-i18n="s6_t">Instalações Técnicas & Conforto</h3>
            <ul class="space-y-2.5 text-sm text-slate-800 flex-1">
              <li class="flex items-start gap-2.5"><i class="fa-solid fa-circle-check text-emerald-700 mt-1"></i><span data-i18n="s6_l1">Instalação e higienização de Ar-Condicionado Split</span></li>
              <li class="flex items-start gap-2.5"><i class="fa-solid fa-circle-check text-emerald-700 mt-1"></i><span data-i18n="s6_l2">Manutenção de bombas de poço artesiano e irrigação</span></li>
              <li class="flex items-start gap-2.5"><i class="fa-solid fa-circle-check text-emerald-700 mt-1"></i><span data-i18n="s6_l3">Câmeras Wi-Fi para monitoramento remoto, refletores solares e verniz em decks</span></li>
            </ul>
          </div>
        </div>
      </div>
    </div>
  </section>

  <!-- ==================== 5 PLANS & COMBOS PRICING ==================== -->
  <section id="planos" class="py-24 bg-brand-dark text-white relative">
    <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
      <div class="text-center max-w-3xl mx-auto mb-12">
        <span class="inline-block bg-emerald-900 border border-emerald-700 text-amber-300 font-extrabold text-xs uppercase tracking-widest px-4 py-1.5 rounded-full" data-i18n="plans_kicker">
          Transparência & Previsibilidade
        </span>
        <h2 class="font-display font-extrabold text-3xl sm:text-4xl lg:text-5xl text-white mt-3" data-i18n="plans_title">
          5 Planos e Combos Sob Medida
        </h2>
        <p class="text-slate-100 mt-3 text-base sm:text-lg leading-relaxed" data-i18n="plans_desc">
          Escolha entre nossas assinaturas mensais de manutenção contínua ou combos fechados para obras e revitalização. Valores de referência para terrenos até 1.000 m².
        </p>

        <!-- Currency Switcher (USD / PYG) -->
        <div class="inline-flex items-center bg-emerald-950 border border-emerald-700 p-1.5 rounded-2xl mt-7 shadow-lg">
          <button onclick="setCurrency('USD')" id="curr-usd" class="px-5 py-2.5 rounded-xl text-sm font-extrabold transition bg-amber-400 text-slate-950 shadow">
            🇺🇸 Dólares (USD $)
          </button>
          <button onclick="setCurrency('PYG')" id="curr-pyg" class="px-5 py-2.5 rounded-xl text-sm font-extrabold transition text-white hover:text-amber-300">
            🇵🇾 Guaraníes (Gs.)
          </button>
        </div>
      </div>

      <!-- Row 1: 3 Monthly Subscription Plans (High-Contrast White Cards on Dark Emerald Section) -->
      <div class="mb-6">
        <h3 class="text-sm uppercase tracking-widest text-amber-300 font-extrabold mb-6 flex items-center gap-2">
          <i class="fa-solid fa-calendar-check"></i>
          <span data-i18n="plans_sub_heading">Assinaturas Mensais Recorrentes (Paz de Espírito o Ano Todo)</span>
        </h3>

        <div class="grid lg:grid-cols-3 gap-7">
          <!-- PLANO 1 -->
          <div class="bg-white text-slate-900 border border-slate-200 rounded-3xl p-7 flex flex-col justify-between shadow-xl card-hover">
            <div>
              <div class="flex items-center justify-between mb-4">
                <span class="text-xs font-extrabold uppercase tracking-wider px-3 py-1 rounded-full bg-slate-100 text-slate-900" data-i18n="pl1_tag">Plano 01 • Essencial</span>
                <span class="text-xs font-bold text-emerald-800" data-i18n="pl1_scope">Piscina + Jardim</span>
              </div>
              <h4 class="font-display font-extrabold text-2xl text-slate-950" data-i18n="pl1_name">Piscina & Jardim</h4>
              <p class="text-slate-700 text-sm mt-2" data-i18n="pl1_desc">Ideal para moradores fixos que desejam área externa sempre limpa e saudável.</p>

              <div class="my-6 pb-6 border-b border-slate-200">
                <div class="font-display font-extrabold text-3xl sm:text-4xl text-emerald-800 price-tag"
                     data-usd="$110 – $140" data-pyg="Gs. 860mil – 1.09M">
                  $110 – $140
                </div>
                <span class="text-xs font-semibold text-slate-700" data-i18n="per_month">/ mês (terrenos até 1.000 m²)</span>
              </div>

              <ul class="space-y-3 text-sm text-slate-800 mb-8">
                <li class="flex items-start gap-2.5"><i class="fa-solid fa-circle-check text-emerald-700 mt-1"></i><span data-i18n="pl1_f1"><strong>4 visitas mensais</strong> de piscina (1x por semana)</span></li>
                <li class="flex items-start gap-2.5"><i class="fa-solid fa-circle-check text-emerald-700 mt-1"></i><span data-i18n="pl1_f2">Controle químico completo + aspiração</span></li>
                <li class="flex items-start gap-2.5"><i class="fa-solid fa-circle-check text-emerald-700 mt-1"></i><span data-i18n="pl1_f3"><strong>2 cortes de grama</strong> e acabamento por mês</span></li>
                <li class="flex items-start gap-2.5"><i class="fa-solid fa-circle-check text-emerald-700 mt-1"></i><span data-i18n="pl1_f4">Poda leve de manutenção de arbustos</span></li>
              </ul>
            </div>

            <button onclick="selectPlanAndScroll('plan1')" class="w-full py-3.5 px-5 rounded-2xl bg-slate-900 hover:bg-emerald-700 text-white font-extrabold text-sm transition flex items-center justify-center gap-2">
              <i class="fa-brands fa-whatsapp text-lg"></i>
              <span data-i18n="btn_choose_plan1">Contratar Plano 1</span>
            </button>
          </div>

          <!-- PLANO 2 (HIGHLIGHTED) -->
          <div class="bg-white text-slate-900 border-4 border-amber-400 rounded-3xl p-7 flex flex-col justify-between relative shadow-2xl card-hover">
            <div class="absolute -top-4 right-6 bg-amber-400 text-slate-950 text-xs font-extrabold uppercase tracking-wider px-4 py-1.5 rounded-full shadow-md" data-i18n="badge_popular">
              ★ Mais Escolhido
            </div>

            <div>
              <div class="flex items-center justify-between mb-4">
                <span class="text-xs font-extrabold uppercase tracking-wider px-3 py-1 rounded-full bg-amber-100 text-amber-950" data-i18n="pl2_tag">Plano 02 • Completo</span>
                <span class="text-xs font-bold text-emerald-800" data-i18n="pl2_scope">Piscina + Jardim + Zeladoria</span>
              </div>
              <h4 class="font-display font-extrabold text-2xl text-slate-950" data-i18n="pl2_name">Quinta Protegida</h4>
              <p class="text-slate-700 text-sm mt-2" data-i18n="pl2_desc">Perfeito para quem mora em Assunção ou no Brasil e usa a quinta nos fins de semana.</p>

              <div class="my-6 pb-6 border-b border-slate-200">
                <div class="font-display font-extrabold text-3xl sm:text-4xl text-emerald-800 price-tag"
                     data-usd="$170 – $220" data-pyg="Gs. 1.32M – 1.71M">
                  $170 – $220
                </div>
                <span class="text-xs font-semibold text-slate-700" data-i18n="per_month">/ mês (terrenos até 1.000 m²)</span>
              </div>

              <ul class="space-y-3 text-sm text-slate-800 mb-8">
                <li class="flex items-start gap-2.5"><i class="fa-solid fa-circle-check text-emerald-700 mt-1"></i><span data-i18n="pl2_f1"><strong>Tudo do Plano 1</strong> (Piscina semanal + Jardim quinzenal)</span></li>
                <li class="flex items-start gap-2.5"><i class="fa-solid fa-circle-check text-emerald-700 mt-1"></i><span data-i18n="pl2_f2"><strong>Zeladoria Semanal:</strong> Abertura da casa para ventilar</span></li>
                <li class="flex items-start gap-2.5"><i class="fa-solid fa-circle-check text-emerald-700 mt-1"></i><span data-i18n="pl2_f3">Checagem de telhado, calhas e bomba de poço</span></li>
                <li class="flex items-start gap-2.5"><i class="fa-solid fa-circle-check text-emerald-700 mt-1"></i><span data-i18n="pl2_f4">Controle preventivo contra formigas <em>ysaú</em></span></li>
                <li class="flex items-start gap-2.5"><i class="fa-solid fa-circle-check text-emerald-700 mt-1"></i><span data-i18n="pl2_f5"><strong>Relatório semanal com fotos</strong> no WhatsApp</span></li>
              </ul>
            </div>

            <button onclick="selectPlanAndScroll('plan2')" class="w-full py-4 px-5 rounded-2xl bg-amber-400 hover:bg-amber-300 text-slate-950 font-extrabold text-sm transition shadow-md flex items-center justify-center gap-2">
              <i class="fa-brands fa-whatsapp text-lg"></i>
              <span data-i18n="btn_choose_plan2">Contratar Plano 2</span>
            </button>
          </div>

          <!-- PLANO 3 -->
          <div class="bg-white text-slate-900 border border-slate-200 rounded-3xl p-7 flex flex-col justify-between shadow-xl card-hover">
            <div>
              <div class="flex items-center justify-between mb-4">
                <span class="text-xs font-extrabold uppercase tracking-wider px-3 py-1 rounded-full bg-slate-900 text-amber-300" data-i18n="pl3_tag">Plano 03 • VIP</span>
                <span class="text-xs font-bold text-emerald-800" data-i18n="pl3_scope">Gestão Total + Faxina</span>
              </div>
              <h4 class="font-display font-extrabold text-2xl text-slate-950" data-i18n="pl3_name">Fim de Semana VIP</h4>
              <p class="text-slate-700 text-sm mt-2" data-i18n="pl3_desc">Padrão hotelaria: você chega na sexta-feira e a casa está limpa, fresca e pronta.</p>

              <div class="my-6 pb-6 border-b border-slate-200">
                <div class="font-display font-extrabold text-3xl sm:text-4xl text-emerald-800 price-tag"
                     data-usd="$280 – $360" data-pyg="Gs. 2.18M – 2.80M">
                  $280 – $360
                </div>
                <span class="text-xs font-semibold text-slate-700" data-i18n="per_month">/ mês (terrenos até 1.000 m²)</span>
              </div>

              <ul class="space-y-3 text-sm text-slate-800 mb-8">
                <li class="flex items-start gap-2.5"><i class="fa-solid fa-circle-check text-emerald-700 mt-1"></i><span data-i18n="pl3_f1"><strong>Tudo do Plano 2</strong> (Piscina + Jardim + Zeladoria)</span></li>
                <li class="flex items-start gap-2.5"><i class="fa-solid fa-circle-check text-emerald-700 mt-1"></i><span data-i18n="pl3_f2"><strong>Faxina leve pré-chegada</strong> toda quinta/sexta-feira</span></li>
                <li class="flex items-start gap-2.5"><i class="fa-solid fa-circle-check text-emerald-700 mt-1"></i><span data-i18n="pl3_f3">Climatização e geladeira ligadas horas antes</span></li>
                <li class="flex items-start gap-2.5"><i class="fa-solid fa-circle-check text-emerald-700 mt-1"></i><span data-i18n="pl3_f4"><strong>1 chamado mensal de Marido de Aluguel</strong> incluso (reparos elétricos/hidráulicos rápidos)</span></li>
              </ul>
            </div>

            <button onclick="selectPlanAndScroll('plan3')" class="w-full py-3.5 px-5 rounded-2xl bg-slate-900 hover:bg-emerald-700 text-white font-extrabold text-sm transition flex items-center justify-center gap-2">
              <i class="fa-brands fa-whatsapp text-lg"></i>
              <span data-i18n="btn_choose_plan3">Contratar Plano 3</span>
            </button>
          </div>
        </div>
      </div>

      <!-- Row 2: 2 Closed Combos (High-Contrast White Cards) -->
      <div class="mt-14">
        <h3 class="text-sm uppercase tracking-widest text-amber-300 font-extrabold mb-6 flex items-center gap-2">
          <i class="fa-solid fa-box-open"></i>
          <span data-i18n="combos_heading">Combos Fechados de Alto Impacto (Pós-Obra & Revitalização)</span>
        </h3>

        <div class="grid md:grid-cols-2 gap-7">
          <!-- COMBO 4 -->
          <div class="bg-white text-slate-900 border border-slate-200 rounded-3xl p-7 sm:p-8 flex flex-col justify-between shadow-xl card-hover">
            <div>
              <div class="flex flex-wrap items-center justify-between gap-2 mb-4">
                <span class="text-xs font-extrabold uppercase tracking-wider px-3 py-1 rounded-full bg-emerald-100 text-emerald-950" data-i18n="cb4_tag">Combo 04 • Pós-Obra</span>
                <span class="text-xs font-bold text-slate-700" data-i18n="cb4_scope">Limpeza Fina + Instalações</span>
              </div>
              <div class="flex flex-col sm:flex-row sm:items-end justify-between gap-4 pb-6 border-b border-slate-200">
                <div>
                  <h4 class="font-display font-extrabold text-2xl text-slate-950" data-i18n="cb4_name">Pacote "Chave na Mão"</h4>
                  <p class="text-slate-700 text-sm mt-1" data-i18n="cb4_desc">Ideal para casas recém-construídas ou pré-mudança (até 150 m²).</p>
                </div>
                <div class="sm:text-right">
                  <div class="font-display font-extrabold text-3xl text-emerald-800 price-tag"
                       data-usd="$420 – $580" data-pyg="Gs. 3.27M – 4.52M">
                    $420 – $580
                  </div>
                  <span class="text-xs font-semibold text-slate-700" data-i18n="closed_package">pacote fechado</span>
                </div>
              </div>

              <ul class="grid sm:grid-cols-2 gap-3 text-sm text-slate-800 my-6">
                <li class="flex items-start gap-2.5"><i class="fa-solid fa-circle-check text-emerald-700 mt-1"></i><span data-i18n="cb4_f1">Limpeza pós-obra fina completa</span></li>
                <li class="flex items-start gap-2.5"><i class="fa-solid fa-circle-check text-emerald-700 mt-1"></i><span data-i18n="cb4_f2">Hidrolavagem de calçadas externas</span></li>
                <li class="flex items-start gap-2.5"><i class="fa-solid fa-circle-check text-emerald-700 mt-1"></i><span data-i18n="cb4_f3">1 diária de instalador (cortinas, TV, espelhos, luminárias)</span></li>
                <li class="flex items-start gap-2.5"><i class="fa-solid fa-circle-check text-emerald-700 mt-1"></i><span data-i18n="cb4_f4">Instalação de até 2 câmeras Wi-Fi</span></li>
              </ul>
            </div>

            <button onclick="selectPlanAndScroll('combo4')" class="w-full py-3.5 px-5 rounded-2xl bg-slate-900 hover:bg-amber-400 hover:text-slate-950 text-white font-extrabold text-sm transition flex items-center justify-center gap-2">
              <i class="fa-brands fa-whatsapp text-lg"></i>
              <span data-i18n="btn_choose_cb4">Solicitar Combo 4</span>
            </button>
          </div>

          <!-- COMBO 5 -->
          <div class="bg-white text-slate-900 border border-slate-200 rounded-3xl p-7 sm:p-8 flex flex-col justify-between shadow-xl card-hover">
            <div>
              <div class="flex flex-wrap items-center justify-between gap-2 mb-4">
                <span class="text-xs font-extrabold uppercase tracking-wider px-3 py-1 rounded-full bg-amber-100 text-amber-950" data-i18n="cb5_tag">Combo 05 • Transformação</span>
                <span class="text-xs font-bold text-slate-700" data-i18n="cb5_scope">Pintura + Jardim + Piscina + Clima</span>
              </div>
              <div class="flex flex-col sm:flex-row sm:items-end justify-between gap-4 pb-6 border-b border-slate-200">
                <div>
                  <h4 class="font-display font-extrabold text-2xl text-slate-950" data-i18n="cb5_name">Revitalização Total de Quinta</h4>
                  <p class="text-slate-700 text-sm mt-1" data-i18n="cb5_desc">Perfeito para pré-temporada de verão ou valorização para venda.</p>
                </div>
                <div class="sm:text-right">
                  <div class="font-display font-extrabold text-3xl text-emerald-800 price-tag"
                       data-usd="$850 – $1.250" data-pyg="Gs. 6.63M – 9.75M">
                    $850 – $1.250
                  </div>
                  <span class="text-xs font-semibold text-slate-700" data-i18n="closed_package">pacote fechado</span>
                </div>
              </div>

              <ul class="grid sm:grid-cols-2 gap-3 text-sm text-slate-800 my-6">
                <li class="flex items-start gap-2.5"><i class="fa-solid fa-circle-check text-emerald-700 mt-1"></i><span data-i18n="cb5_f1">Hidrolavagem de telhado e muros</span></li>
                <li class="flex items-start gap-2.5"><i class="fa-solid fa-circle-check text-emerald-700 mt-1"></i><span data-i18n="cb5_f2">Pintura externa de fachada/muros (até 120 m²)</span></li>
                <li class="flex items-start gap-2.5"><i class="fa-solid fa-circle-check text-emerald-700 mt-1"></i><span data-i18n="cb5_f3">Poda pesada, adubação e tratamento de choque na piscina</span></li>
                <li class="flex items-start gap-2.5"><i class="fa-solid fa-circle-check text-emerald-700 mt-1"></i><span data-i18n="cb5_f4">Higienização de até 3 aparelhos de Ar-Condicionado</span></li>
              </ul>
            </div>

            <button onclick="selectPlanAndScroll('combo5')" class="w-full py-3.5 px-5 rounded-2xl bg-slate-900 hover:bg-amber-400 hover:text-slate-950 text-white font-extrabold text-sm transition flex items-center justify-center gap-2">
              <i class="fa-brands fa-whatsapp text-lg"></i>
              <span data-i18n="btn_choose_cb5">Solicitar Combo 5</span>
            </button>
          </div>
        </div>
      </div>

      <!-- Footnote -->
      <p class="text-center text-xs sm:text-sm text-slate-200 mt-10 font-medium" data-i18n="plans_footnote">
        * Para quintas com terrenos acima de 1.000 m² (2.500 m² a 5.000 m²), aplicamos um adicional proporcional de $30 a $60 USD/mês referente à roçada extra. Consulte condições com IVA incluído.
      </p>
    </div>
  </section>

  <!-- ==================== HOW IT WORKS (3 STEPS) ==================== -->
  <section id="como-funciona" class="py-20 bg-white">
    <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
      <div class="text-center max-w-2xl mx-auto mb-14">
        <span class="inline-block bg-emerald-100 text-emerald-900 font-extrabold text-xs uppercase tracking-widest px-3.5 py-1.5 rounded-full" data-i18n="how_kicker">
          Processo Simples & Profissional
        </span>
        <h2 class="font-display font-extrabold text-3xl sm:text-4xl text-slate-950 mt-3" data-i18n="how_title">
          Como funciona o nosso atendimento
        </h2>
      </div>

      <div class="grid md:grid-cols-3 gap-8">
        <div class="bg-slate-50 rounded-3xl p-8 border border-slate-200">
          <div class="w-12 h-12 rounded-2xl bg-brand-dark text-amber-300 font-display font-extrabold text-xl flex items-center justify-center mb-5 shadow-sm">
            1
          </div>
          <h3 class="font-display font-extrabold text-xl text-slate-950 mb-2" data-i18n="step1_t">Vistoria & Orçamento Claro</h3>
          <p class="text-slate-700 text-sm leading-relaxed" data-i18n="step1_d">
            Você chama no WhatsApp, agendamos uma visita técnica em Hugua Hú ou região e enviamos uma proposta detalhada por escrito, sem surpresas.
          </p>
        </div>

        <div class="bg-slate-50 rounded-3xl p-8 border border-slate-200">
          <div class="w-12 h-12 rounded-2xl bg-brand-dark text-amber-300 font-display font-extrabold text-xl flex items-center justify-center mb-5 shadow-sm">
            2
          </div>
          <h3 class="font-display font-extrabold text-xl text-slate-950 mb-2" data-i18n="step2_t">Execução Supervisionada</h3>
          <p class="text-slate-700 text-sm leading-relaxed" data-i18n="step2_d">
            Nossa equipe uniformizada ou especialistas credenciados executam o serviço com equipamentos profissionais e supervisão rigorosa de qualidade.
          </p>
        </div>

        <div class="bg-slate-50 rounded-3xl p-8 border border-slate-200">
          <div class="w-12 h-12 rounded-2xl bg-brand-dark text-amber-300 font-display font-extrabold text-xl flex items-center justify-center mb-5 shadow-sm">
            3
          </div>
          <h3 class="font-display font-extrabold text-xl text-slate-950 mb-2" data-i18n="step3_t">Entrega & Relatório Fotográfico</h3>
          <p class="text-slate-700 text-sm leading-relaxed" data-i18n="step3_d">
            Entregamos tudo limpo, enviamos as fotos do resultado pelo WhatsApp e emitimos sua Factura Legal com garantia formal do serviço.
          </p>
        </div>
      </div>
    </div>
  </section>

  <!-- ==================== CONTACT & INSTANT QUOTE CALCULATOR ==================== -->
  <section id="orcamento" class="py-20 bg-slate-100 border-t border-slate-200">
    <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
      <div class="bg-white rounded-[2rem] shadow-xl border border-slate-200 overflow-hidden grid lg:grid-cols-12">
        <!-- Left Info Panel -->
        <div class="lg:col-span-5 bg-brand-dark text-white p-8 sm:p-12 flex flex-col justify-between">
          <div>
            <span class="inline-block bg-emerald-900 text-amber-300 font-extrabold text-xs uppercase tracking-widest px-3.5 py-1.5 rounded-full" data-i18n="form_kicker">
              Atendimento Bilíngue (PT / ES)
            </span>
            <h2 class="font-display font-extrabold text-3xl sm:text-4xl text-white mt-3 leading-tight" data-i18n="form_title">
              Solicite sua Visita ou Orçamento Agora
            </h2>
            <p class="text-slate-100 mt-4 text-sm sm:text-base leading-relaxed" data-i18n="form_desc">
              Preencha os dados ao lado para gerar seu pedido formatado e iniciar o atendimento imediato pelo WhatsApp com a equipe da <strong class="text-amber-300">A Rocha Gestão e Serviços</strong>.
            </p>

            <div class="space-y-4 mt-8 pt-8 border-t border-emerald-800 text-sm">
              <div class="flex items-start gap-3.5">
                <div class="w-9 h-9 rounded-xl bg-emerald-900 flex items-center justify-center text-amber-300 shrink-0">
                  <i class="fa-solid fa-location-dot"></i>
                </div>
                <div>
                  <p class="font-bold text-white" data-i18n="info1_t">Base & Área de Cobertura</p>
                  <p class="text-slate-200" data-i18n="info1_d">Sede em Hugua Hú • Atendimento em Atyrá, Altos, Caacupé, Tobatí e San Bernardino.</p>
                </div>
              </div>

              <div class="flex items-start gap-3.5">
                <div class="w-9 h-9 rounded-xl bg-emerald-900 flex items-center justify-center text-amber-300 shrink-0">
                  <i class="fa-solid fa-clock"></i>
                </div>
                <div>
                  <p class="font-bold text-white" data-i18n="info2_t">Horário de Atendimento</p>
                  <p class="text-slate-200" data-i18n="info2_d">Segunda a Sábado: 07:30 às 18:00 (Plantão emergencial para assinantes).</p>
                </div>
              </div>

              <div class="flex items-start gap-3.5">
                <div class="w-9 h-9 rounded-xl bg-emerald-900 flex items-center justify-center text-amber-300 shrink-0">
                  <i class="fa-solid fa-shield-halved"></i>
                </div>
                <div>
                  <p class="font-bold text-white" data-i18n="info3_t">Garantia & Formalidade</p>
                  <p class="text-slate-200" data-i18n="info3_d">Emissão de Factura Legal (IVA) e contrato transparente para planos mensais.</p>
                </div>
              </div>
            </div>
          </div>

          <div class="mt-10 pt-6 border-t border-emerald-800 flex items-center gap-3 text-xs text-slate-200">
            <i class="fa-solid fa-bolt text-amber-300 text-base"></i>
            <span data-i18n="form_fast">Tempo médio de resposta no WhatsApp: <strong class="text-white">menos de 15 minutos</strong>.</span>
          </div>
        </div>

        <!-- Right Interactive Form -->
        <div class="lg:col-span-7 p-8 sm:p-12 bg-white">
          <form id="quoteForm" onsubmit="handleQuoteSubmit(event)" class="space-y-5">
            <div class="grid sm:grid-cols-2 gap-5">
              <div>
                <label class="block text-xs font-extrabold uppercase tracking-wider text-slate-800 mb-2" data-i18n="lbl_name">Seu Nome *</label>
                <input type="text" id="clientName" required placeholder="Ex: Carlos Silva"
                       class="w-full px-4 py-3.5 rounded-xl border border-slate-300 text-slate-900 placeholder:text-slate-500 focus:ring-2 focus:ring-emerald-700 focus:border-emerald-700 outline-none text-sm" />
              </div>

              <div>
                <label class="block text-xs font-extrabold uppercase tracking-wider text-slate-800 mb-2" data-i18n="lbl_city">Cidade / Região da Propriedade *</label>
                <select id="clientCity" class="w-full px-4 py-3.5 rounded-xl border border-slate-300 text-slate-900 focus:ring-2 focus:ring-emerald-700 focus:border-emerald-700 outline-none text-sm bg-white">
                  <option value="Hugua Hú">Hugua Hú</option>
                  <option value="Atyrá">Atyrá</option>
                  <option value="Altos">Altos</option>
                  <option value="San Bernardino">San Bernardino</option>
                  <option value="Caacupé">Caacupé</option>
                  <option value="Tobatí / Cordillera" data-i18n="opt_other_city">Tobatí / Outra em Cordillera</option>
                </select>
              </div>
            </div>

            <div class="grid sm:grid-cols-2 gap-5">
              <div>
                <label class="block text-xs font-extrabold uppercase tracking-wider text-slate-800 mb-2" data-i18n="lbl_plan">Plano ou Serviço Desejado *</label>
                <select id="selectedPlan" class="w-full px-4 py-3.5 rounded-xl border border-slate-300 text-slate-900 focus:ring-2 focus:ring-emerald-700 focus:border-emerald-700 outline-none text-sm bg-white">
                  <option value="plan1" data-i18n="opt_p1">Plano 1: Piscina & Jardim ($110–$140/mês)</option>
                  <option value="plan2" selected data-i18n="opt_p2">Plano 2: Quinta Protegida ($170–$220/mês) ★</option>
                  <option value="plan3" data-i18n="opt_p3">Plano 3: Fim de Semana VIP ($280–$360/mês)</option>
                  <option value="combo4" data-i18n="opt_c4">Combo 4: Pacote Chave na Mão ($420–$580)</option>
                  <option value="combo5" data-i18n="opt_c5">Combo 5: Revitalização Total ($850–$1.250)</option>
                  <option value="single" data-i18n="opt_single">Serviço Avulso (Reforma / Pintura / Manutenção)</option>
                  <option value="postwork" data-i18n="opt_post">Limpeza Pós-Obra Avulsa</option>
                </select>
              </div>

              <div>
                <label class="block text-xs font-extrabold uppercase tracking-wider text-slate-800 mb-2" data-i18n="lbl_size">Tamanho Aproximado do Terreno</label>
                <select id="propertySize" class="w-full px-4 py-3.5 rounded-xl border border-slate-300 text-slate-900 focus:ring-2 focus:ring-emerald-700 focus:border-emerald-700 outline-none text-sm bg-white">
                  <option value="size1" data-i18n="opt_s1">Até 1.000 m² (Padrão)</option>
                  <option value="size2" data-i18n="opt_s2">1.000 m² a 2.500 m²</option>
                  <option value="size3" data-i18n="opt_s3">2.500 m² a 5.000 m² (Quinta Média)</option>
                  <option value="size4" data-i18n="opt_s4">Acima de 5.000 m² (Chácara Grande)</option>
                </select>
              </div>
            </div>

            <div>
              <label class="block text-xs font-extrabold uppercase tracking-wider text-slate-800 mb-2" data-i18n="lbl_notes">Detalhes do que você precisa (Opcional)</label>
              <textarea id="clientNotes" rows="3" placeholder="Ex: Tenho uma quinta em Hugua Hú com piscina de 8x4m, preciso de manutenção semanal e pintura do muro..."
                        class="w-full px-4 py-3 rounded-xl border border-slate-300 text-slate-900 placeholder:text-slate-500 focus:ring-2 focus:ring-emerald-700 focus:border-emerald-700 outline-none text-sm"></textarea>
            </div>

            <button type="submit" class="w-full py-4 px-6 rounded-2xl bg-emerald-700 hover:bg-emerald-600 text-white font-extrabold text-base shadow-lg transition flex items-center justify-center gap-3">
              <i class="fa-brands fa-whatsapp text-2xl"></i>
              <span data-i18n="btn_submit">Enviar Pedido pelo WhatsApp Agora</span>
            </button>
          </form>
        </div>
      </div>
    </div>
  </section>

  <!-- ==================== FOOTER ==================== -->
  <footer class="bg-brand-dark text-slate-200 py-12 border-t border-emerald-900">
    <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 flex flex-col md:flex-row items-center justify-between gap-6">
      <div class="flex items-center gap-3">
        <div class="w-9 h-9 rounded-xl bg-amber-400 text-slate-950 flex items-center justify-center font-extrabold">
          <i class="fa-solid fa-mountain-sun"></i>
        </div>
        <div>
          <p class="text-white font-display font-extrabold text-sm" data-i18n="footer_brand">A ROCHA GESTÃO E SERVIÇOS</p>
          <p class="text-xs text-slate-300">Hugua Hú • Cordillera • Paraguay</p>
        </div>
      </div>

      <p class="text-xs text-slate-300 text-center md:text-right" data-i18n="footer_copy">
        © 2026 A Rocha Gestão e Serviços. Todos os direitos reservados. • Factura Legal & Garantia Técnica.
      </p>
    </div>
  </footer>

  <!-- ==================== FLOATING WHATSAPP BUTTON ==================== -->
  <a id="floatingWaBtn" href="https://wa.me/595981000000?text=Ol%C3%A1!%20Gostaria%20de%20um%20or%C3%A7amento%20da%20A%20Rocha%20Gest%C3%A3o%20e%20Servi%C3%A7os."
     target="_blank" rel="noopener noreferrer"
     aria-label="Falar no WhatsApp"
     class="fixed bottom-6 right-6 z-50 bg-emerald-600 hover:bg-emerald-500 text-white rounded-full p-4 shadow-2xl flex items-center justify-center transition transform hover:scale-110">
    <i class="fa-brands fa-whatsapp text-3xl"></i>
  </a>

  <!-- ==================== CUSTOM CONFIRMATION MODAL (NO ALERT) ==================== -->
  <div id="quoteModal" class="hidden fixed inset-0 z-50 bg-black/75 backdrop-blur-sm flex items-center justify-center p-4">
    <div class="bg-white rounded-3xl max-w-md w-full p-7 shadow-2xl space-y-5 border border-slate-200">
      <div class="flex items-center justify-between">
        <div class="flex items-center gap-3">
          <div class="w-11 h-11 rounded-2xl bg-emerald-100 text-emerald-800 flex items-center justify-center text-xl">
            <i class="fa-brands fa-whatsapp"></i>
          </div>
          <h3 class="font-display font-extrabold text-lg text-slate-950" data-i18n="modal_title">Resumo Pronto para Envio</h3>
        </div>
        <button onclick="closeQuoteModal()" class="text-slate-600 hover:text-slate-950 p-1">
          <i class="fa-solid fa-xmark text-xl"></i>
        </button>
      </div>

      <div id="modalSummaryText" class="bg-slate-100 rounded-2xl p-4 text-xs sm:text-sm text-slate-900 whitespace-pre-line font-mono border border-slate-300"></div>

      <div class="flex flex-col sm:flex-row gap-3">
        <a id="modalWhatsappLink" href="#" target="_blank" rel="noopener noreferrer"
           class="flex-1 py-3.5 px-4 rounded-xl bg-emerald-700 hover:bg-emerald-600 text-white font-extrabold text-sm text-center flex items-center justify-center gap-2">
          <i class="fa-brands fa-whatsapp text-lg"></i>
          <span data-i18n="modal_btn_wa">Abrir WhatsApp</span>
        </a>
        <button onclick="closeQuoteModal()" class="py-3.5 px-4 rounded-xl bg-slate-200 hover:bg-slate-300 text-slate-900 font-bold text-sm" data-i18n="modal_btn_close">
          Fechar
        </button>
      </div>
    </div>
  </div>

  <!-- ==================== JAVASCRIPT INTERACTIVITY & FULL BILINGUAL ENGINE ==================== -->
  <script>
    let currentLang = 'pt';

    // Mobile Menu Toggle
    const mobileMenuBtn = document.getElementById('mobile-menu-btn');
    const mobileMenu = document.getElementById('mobile-menu');
    mobileMenuBtn.addEventListener('click', () => {
      mobileMenu.classList.toggle('hidden');
    });
    function closeMobileMenu() {
      mobileMenu.classList.add('hidden');
    }

    // Currency Switcher (USD vs PYG)
    function setCurrency(currency) {
      const btnUsd = document.getElementById('curr-usd');
      const btnPyg = document.getElementById('curr-pyg');
      const priceTags = document.querySelectorAll('.price-tag');

      if (currency === 'USD') {
        btnUsd.className = 'px-5 py-2.5 rounded-xl text-sm font-extrabold transition bg-amber-400 text-slate-950 shadow';
        btnPyg.className = 'px-5 py-2.5 rounded-xl text-sm font-extrabold transition text-white hover:text-amber-300';
        priceTags.forEach(el => el.textContent = el.getAttribute('data-usd'));
      } else {
        btnPyg.className = 'px-5 py-2.5 rounded-xl text-sm font-extrabold transition bg-amber-400 text-slate-950 shadow';
        btnUsd.className = 'px-5 py-2.5 rounded-xl text-sm font-extrabold transition text-white hover:text-amber-300';
        priceTags.forEach(el => el.textContent = el.getAttribute('data-pyg'));
      }
    }

    // Select Plan Button -> Pre-fill Form & Smooth Scroll
    function selectPlanAndScroll(planValue) {
      const selectEl = document.getElementById('selectedPlan');
      selectEl.value = planValue;
      document.getElementById('orcamento').scrollIntoView({ behavior: 'smooth' });
    }

    // Handle Quote Form Submission
    function handleQuoteSubmit(event) {
      event.preventDefault();
      const name = document.getElementById('clientName').value.trim();
      const city = document.getElementById('clientCity').value;
      const planSelect = document.getElementById('selectedPlan');
      const planText = planSelect.options[planSelect.selectedIndex].text;
      const sizeSelect = document.getElementById('propertySize');
      const sizeText = sizeSelect.options[sizeSelect.selectedIndex].text;
      const notes = document.getElementById('clientNotes').value.trim();

      // Replace with your real Paraguayan WhatsApp number (e.g., 595981123456)
      const companyPhone = '595981000000';

      let message = '';
      if (currentLang === 'pt') {
        message =
          `Olá, A Rocha Gestão e Serviços! Gostaria de solicitar um orçamento:\n\n` +
          `• *Nome:* ${name}\n` +
          `• *Região:* ${city}\n` +
          `• *Interesse:* ${planText}\n` +
          `• *Terreno:* ${sizeText}\n` +
          (notes ? `• *Detalhes:* ${notes}` : '');
      } else {
        message =
          `¡Hola, A Rocha Gestión y Servicios! Quisiera solicitar un presupuesto:\n\n` +
          `• *Nombre:* ${name}\n` +
          `• *Zona:* ${city}\n` +
          `• *Interés:* ${planText}\n` +
          `• *Terreno:* ${sizeText}\n` +
          (notes ? `• *Detalles:* ${notes}` : '');
      }

      const encodedMsg = encodeURIComponent(message);
      const waUrl = `https://wa.me/${companyPhone}?text=${encodedMsg}`;

      document.getElementById('modalSummaryText').textContent = message;
      document.getElementById('modalWhatsappLink').href = waUrl;
      document.getElementById('quoteModal').classList.remove('hidden');
    }

    function closeQuoteModal() {
      document.getElementById('quoteModal').classList.add('hidden');
    }

    // Complete 100% Bilingual Dictionary (Português / Español)
    const translations = {
      pt: {
        brand_sub: 'Gestão e Serviços',
        nav_why: 'Diferenciais',
        nav_services: 'Nossos Serviços',
        nav_plans: 'Planos & Preços',
        nav_how: 'Como Funciona',
        nav_contact: 'Orçamento',
        nav_cta: 'Solicitar Orçamento',
        hero_badge: 'Hugua Hú • Atyrá • Altos • Caacupé • San Bernardino',
        hero_title: 'Sua Casa ou Quinta Sempre Impecável. <span class="text-amber-300">Tudo em Um Só Lugar.</span>',
        hero_subtitle: 'Na <strong class="text-white font-bold">A Rocha Gestão e Serviços</strong>, cuidamos de reformas rápidas ("Marido de Aluguel"), limpeza pós-obra, jardinagem, manutenção de piscinas e zeladoria semanal com <strong class="text-amber-300 font-semibold">relatórios por foto no WhatsApp</strong> e <strong class="text-white font-semibold">Factura Legal</strong>.',
        hero_btn_plans: 'Ver 5 Planos e Preços',
        hero_btn_quote: 'Orçamento Rápido',
        stat_1_v: 'Gestão Total',
        stat_1: 'Manutenção e obras',
        stat_2_v: '100% Visual',
        stat_2: 'Relatório com fotos',
        stat_3_v: 'Factura Legal',
        stat_3: 'Empresa formalizada',
        card_report_title: 'Relatório Semanal de Quinta',
        card_report_sub: 'Piscina tratada, grama cortada e casa ventilada',
        card_status: 'Pronta para o Fim de Semana',
        why_kicker: 'Por que contratar a A Rocha?',
        why_title: 'Acabamos com a dor de cabeça de gerenciar vários prestadores',
        why_desc: 'Sabemos como é difícil encontrar mão de obra pontual e confiável no interior. Criamos uma gestão profissional com padrão empresarial para cuidar do seu patrimônio.',
        adv_1_t: 'Pontualidade & Compromisso',
        adv_1_d: 'Cronograma rígido de visitas e prazos de entrega cumpridos à risca. Sem sumiços no meio da obra ou desculpas.',
        adv_2_t: 'Relatórios Visuais no WhatsApp',
        adv_2_d: 'Mora em Assunção ou no Brasil? Receba fotos do antes e depois a cada visita semanal da nossa equipe na sua quinta.',
        adv_3_t: '1 Único Contato Resolve Tudo',
        adv_3_d: 'Do corte de grama e limpeza da piscina até pintura, elétrica, ar-condicionado e limpeza pós-obra sob uma única gestão.',
        adv_4_t: 'Garantia & Factura Legal',
        adv_4_d: 'Empresa formalizada no Paraguai, equipe uniformizada, supervisão técnica e emissão de Factura para sua segurança.',
        srv_kicker: 'Soluções Completas para Casas e Quintas',
        srv_title: 'Tudo o que Sua Propriedade Precisa em Um Só Lugar',
        srv_desc: 'Contamos com equipe própria polivalente e especialistas técnicos credenciados para cada tipo de demanda na sua residência ou chácara.',
        srv_link: 'Solicitar serviço avulso',
        s1_badge: 'Mais Procurado',
        s1_t: 'Reformas Simples & Marido de Aluguel',
        s1_l1: 'Pintura residencial e comercial (interna e externa)',
        s1_l2: 'Reparos de alvenaria, reboco, pisos e rejuntamento',
        s1_l3: 'Instalação de drywall, forros e divisórias',
        s1_l4: 'Elétrica e hidráulica básica (torneiras, chuveiros, tomadas, luminárias)',
        s1_l5: 'Montagem de móveis, cortinas, suportes de TV e prateleiras',
        s2_badge: 'Alta Precisão',
        s2_t: 'Limpeza Especializada & Pós-Obra',
        s2_l1: '<strong>Limpeza Pós-Obra Fina:</strong> Remoção técnica de tinta, cimento e poeira sem riscar porcelanatos',
        s2_l2: 'Faxina pesada pré e pós-mudança',
        s2_l3: 'Hidrolavagem de telhados coloniais, muros de pedra, decks e calçadas',
        s3_badge: 'Áreas Verdes',
        s3_t: 'Jardinagem & Áreas Externas',
        s3_l1: 'Corte de grama, acabamento de bordas e poda de árvores/arbustos',
        s3_l2: 'Roçada pesada e limpeza de terrenos e lotes fechados',
        s3_l3: 'Adubação e controle preventivo de pragas (formigas <em>ysaú</em> e cupins)',
        s4_badge: 'Água Cristalina',
        s4_t: 'Manutenção Completa de Piscinas',
        s4_l1: 'Aspiração, peneiramento e escovação semanal de bordas',
        s4_l2: 'Controle químico rigoroso (pH, cloro, alcalinidade e algicida)',
        s4_l3: 'Manutenção preventiva de bomba, filtro e casa de máquinas',
        s5_badge: 'Exclusivo Quintas',
        s5_t: 'Zeladoria & "Casa Pronta"',
        s5_l1: 'Vistoria semanal, abertura para ventilação e checagem pós-chuva',
        s5_l2: '<strong>Preparação Pré-Chegada:</strong> Ligamos geladeira, ar-condicionado e luzes antes da sua família chegar na sexta-feira',
        s5_l3: 'Relatório semanal com fotos enviado no WhatsApp',
        s6_badge: 'Conforto & Técnica',
        s6_t: 'Instalações Técnicas & Conforto',
        s6_l1: 'Instalação e higienização de Ar-Condicionado Split',
        s6_l2: 'Manutenção de bombas de poço artesiano e irrigação',
        s6_l3: 'Câmeras Wi-Fi para monitoramento remoto, refletores solares e verniz em decks',
        plans_kicker: 'Transparência & Previsibilidade',
        plans_title: '5 Planos e Combos Sob Medida',
        plans_desc: 'Escolha entre nossas assinaturas mensais de manutenção contínua ou combos fechados para obras e revitalização. Valores de referência para terrenos até 1.000 m².',
        plans_sub_heading: 'Assinaturas Mensais Recorrentes (Paz de Espírito o Ano Todo)',
        per_month: '/ mês (terrenos até 1.000 m²)',
        closed_package: 'pacote fechado',
        badge_popular: '★ Mais Escolhido',
        pl1_tag: 'Plano 01 • Essencial',
        pl1_scope: 'Piscina + Jardim',
        pl1_name: 'Piscina & Jardim',
        pl1_desc: 'Ideal para moradores fixos que desejam área externa sempre limpa e saudável.',
        pl1_f1: '<strong>4 visitas mensais</strong> de piscina (1x por semana)',
        pl1_f2: 'Controle químico completo + aspiração',
        pl1_f3: '<strong>2 cortes de grama</strong> e acabamento por mês',
        pl1_f4: 'Poda leve de manutenção de arbustos',
        btn_choose_plan1: 'Contratar Plano 1',
        pl2_tag: 'Plano 02 • Completo',
        pl2_scope: 'Piscina + Jardim + Zeladoria',
        pl2_name: 'Quinta Protegida',
        pl2_desc: 'Perfeito para quem mora em Assunção ou no Brasil e usa a quinta nos fins de semana.',
        pl2_f1: '<strong>Tudo do Plano 1</strong> (Piscina semanal + Jardim quinzenal)',
        pl2_f2: '<strong>Zeladoria Semanal:</strong> Abertura da casa para ventilar',
        pl2_f3: 'Checagem de telhado, calhas e bomba de poço',
        pl2_f4: 'Controle preventivo contra formigas <em>ysaú</em>',
        pl2_f5: '<strong>Relatório semanal com fotos</strong> no WhatsApp',
        btn_choose_plan2: 'Contratar Plano 2',
        pl3_tag: 'Plano 03 • VIP',
        pl3_scope: 'Gestão Total + Faxina',
        pl3_name: 'Fim de Semana VIP',
        pl3_desc: 'Padrão hotelaria: você chega na sexta-feira e a casa está limpa, fresca e pronta.',
        pl3_f1: '<strong>Tudo do Plano 2</strong> (Piscina + Jardim + Zeladoria)',
        pl3_f2: '<strong>Faxina leve pré-chegada</strong> toda quinta/sexta-feira',
        pl3_f3: 'Climatização e geladeira ligadas horas antes',
        pl3_f4: '<strong>1 chamado mensal de Marido de Aluguel</strong> incluso (reparos elétricos/hidráulicos rápidos)',
        btn_choose_plan3: 'Contratar Plano 3',
        combos_heading: 'Combos Fechados de Alto Impacto (Pós-Obra & Revitalização)',
        cb4_tag: 'Combo 04 • Pós-Obra',
        cb4_scope: 'Limpeza Fina + Instalações',
        cb4_name: 'Pacote "Chave na Mão"',
        cb4_desc: 'Ideal para casas recém-construídas ou pré-mudança (até 150 m²).',
        cb4_f1: 'Limpeza pós-obra fina completa',
        cb4_f2: 'Hidrolavagem de calçadas externas',
        cb4_f3: '1 diária de instalador (cortinas, TV, espelhos, luminárias)',
        cb4_f4: 'Instalação de até 2 câmeras Wi-Fi',
        btn_choose_cb4: 'Solicitar Combo 4',
        cb5_tag: 'Combo 05 • Transformação',
        cb5_scope: 'Pintura + Jardim + Piscina + Clima',
        cb5_name: 'Revitalização Total de Quinta',
        cb5_desc: 'Perfeito para pré-temporada de verão ou valorização para venda.',
        cb5_f1: 'Hidrolavagem de telhado e muros',
        cb5_f2: 'Pintura externa de fachada/muros (até 120 m²)',
        cb5_f3: 'Poda pesada, adubação e tratamento de choque na piscina',
        cb5_f4: 'Higienização de até 3 aparelhos de Ar-Condicionado',
        btn_choose_cb5: 'Solicitar Combo 5',
        plans_footnote: '* Para quintas com terrenos acima de 1.000 m² (2.500 m² a 5.000 m²), aplicamos um adicional proporcional de $30 a $60 USD/mês referente à roçada extra. Consulte condições com IVA incluído.',
        how_kicker: 'Processo Simples & Profissional',
        how_title: 'Como funciona o nosso atendimento',
        step1_t: 'Vistoria & Orçamento Claro',
        step1_d: 'Você chama no WhatsApp, agendamos uma visita técnica em Hugua Hú ou região e enviamos uma proposta detalhada por escrito, sem surpresas.',
        step2_t: 'Execução Supervisionada',
        step2_d: 'Nossa equipe uniformizada ou especialistas credenciados executam o serviço com equipamentos profissionais e supervisão rigorosa de qualidade.',
        step3_t: 'Entrega & Relatório Fotográfico',
        step3_d: 'Entregamos tudo limpo, enviamos as fotos do resultado pelo WhatsApp e emitimos sua Factura Legal com garantia formal do serviço.',
        form_kicker: 'Atendimento Bilíngue (PT / ES)',
        form_title: 'Solicite sua Visita ou Orçamento Agora',
        form_desc: 'Preencha os dados ao lado para gerar seu pedido formatado e iniciar o atendimento imediato pelo WhatsApp com a equipe da <strong class="text-amber-300">A Rocha Gestão e Serviços</strong>.',
        info1_t: 'Base & Área de Cobertura',
        info1_d: 'Sede em Hugua Hú • Atendimento em Atyrá, Altos, Caacupé, Tobatí e San Bernardino.',
        info2_t: 'Horário de Atendimento',
        info2_d: 'Segunda a Sábado: 07:30 às 18:00 (Plantão emergencial para assinantes).',
        info3_t: 'Garantia & Formalidade',
        info3_d: 'Emissão de Factura Legal (IVA) e contrato transparente para planos mensais.',
        form_fast: 'Tempo médio de resposta no WhatsApp: <strong class="text-white">menos de 15 minutos</strong>.',
        lbl_name: 'Seu Nome *',
        lbl_city: 'Cidade / Região da Propriedade *',
        opt_other_city: 'Tobatí / Outra em Cordillera',
        lbl_plan: 'Plano ou Serviço Desejado *',
        opt_p1: 'Plano 1: Piscina & Jardim ($110–$140/mês)',
        opt_p2: 'Plano 2: Quinta Protegida ($170–$220/mês) ★',
        opt_p3: 'Plano 3: Fim de Semana VIP ($280–$360/mês)',
        opt_c4: 'Combo 4: Pacote Chave na Mão ($420–$580)',
        opt_c5: 'Combo 5: Revitalização Total ($850–$1.250)',
        opt_single: 'Serviço Avulso (Reforma / Pintura / Manutenção)',
        opt_post: 'Limpeza Pós-Obra Avulsa',
        lbl_size: 'Tamanho Aproximado do Terreno',
        opt_s1: 'Até 1.000 m² (Padrão)',
        opt_s2: '1.000 m² a 2.500 m²',
        opt_s3: '2.500 m² a 5.000 m² (Quinta Média)',
        opt_s4: 'Acima de 5.000 m² (Chácara Grande)',
        lbl_notes: 'Detalhes do que você precisa (Opcional)',
        btn_submit: 'Enviar Pedido pelo WhatsApp Agora',
        footer_brand: 'A ROCHA GESTÃO E SERVIÇOS',
        footer_copy: '© 2026 A Rocha Gestão e Serviços. Todos os direitos reservados. • Factura Legal & Garantia Técnica.',
        modal_title: 'Resumo Pronto para Envio',
        modal_btn_wa: 'Abrir WhatsApp',
        modal_btn_close: 'Fechar'
      },
      es: {
        brand_sub: 'Gestión y Servicios',
        nav_why: 'Diferenciales',
        nav_services: 'Nuestros Servicios',
        nav_plans: 'Planes y Precios',
        nav_how: 'Cómo Funciona',
        nav_contact: 'Presupuesto',
        nav_cta: 'Pedir Presupuesto',
        hero_badge: 'Hugua Hú • Atyrá • Altos • Caacupé • San Bernardino',
        hero_title: 'Su Casa o Quinta Siempre Impecable. <span class="text-amber-300">Todo en Un Solo Lugar.</span>',
        hero_subtitle: 'En <strong class="text-white font-bold">A Rocha Gestión y Servicios</strong> nos encargamos de reformas rápidas, limpieza post-obra, jardinería, mantenimiento de piscinas y casero semanal con <strong class="text-amber-300 font-semibold">reportes con fotos por WhatsApp</strong> y <strong class="text-white font-semibold">Factura Legal</strong>.',
        hero_btn_plans: 'Ver 5 Planes y Precios',
        hero_btn_quote: 'Presupuesto Rápido',
        stat_1_v: 'Gestión Total',
        stat_1: 'Mantenimiento y obras',
        stat_2_v: '100% Visual',
        stat_2: 'Reporte con fotos',
        stat_3_v: 'Factura Legal',
        stat_3: 'Empresa formalizada',
        card_report_title: 'Reporte Semanal de Quinta',
        card_report_sub: 'Piscina tratada, pasto cortado y casa ventilada',
        card_status: 'Lista para el Fin de Semana',
        why_kicker: '¿Por qué contratar a A Rocha?',
        why_title: 'Eliminamos el dolor de cabeza de coordinar varios proveedores',
        why_desc: 'Sabemos lo difícil que es encontrar mano de obra puntual y confiable en el interior. Creamos una gestión profesional con estándar empresarial para cuidar su propiedad.',
        adv_1_t: 'Puntualidad y Compromiso',
        adv_1_d: 'Cronograma estricto de visitas y plazos de entrega cumplidos al pie de la letra. Sin ausencias en medio de la obra ni excusas.',
        adv_2_t: 'Reportes Visuales por WhatsApp',
        adv_2_d: '¿Vive en Asunción o en el exterior? Reciba fotos del antes y después en cada visita semanal de nuestro equipo a su quinta.',
        adv_3_t: '1 Solo Contacto Resuelve Todo',
        adv_3_d: 'Desde el corte de pasto y limpieza de piscina hasta pintura, electricidad, aire acondicionado y limpieza post-obra bajo una única gestión.',
        adv_4_t: 'Garantía y Factura Legal',
        adv_4_d: 'Empresa formalizada en Paraguay, equipo uniformado, supervisión técnica y emisión de Factura para su tranquilidad.',
        srv_kicker: 'Soluciones Integrales para Casas y Quintas',
        srv_title: 'Todo lo que Su Propiedad Necesita en Un Solo Lugar',
        srv_desc: 'Contamos con equipo propio polivalente y especialistas técnicos acreditados para cada necesidad en su residencia o quinta.',
        srv_link: 'Solicitar servicio puntual',
        s1_badge: 'Más Solicitado',
        s1_t: 'Reformas Simples y Mantenimiento Rápido',
        s1_l1: 'Pintura residencial y comercial (interior y exterior)',
        s1_l2: 'Reparaciones de albañilería, revoque, pisos y juntas',
        s1_l3: 'Instalación de durlock/yeso, cielorrasos y divisorias',
        s1_l4: 'Electricidad y plomería básica (grifos, duchas, tomas, luminarias)',
        s1_l5: 'Armado de muebles, cortinas, soportes de TV y estantes',
        s2_badge: 'Alta Precisión',
        s2_t: 'Limpieza Especializada y Post-Obra',
        s2_l1: '<strong>Limpieza Post-Obra Fina:</strong> Remoción técnica de pintura, cemento y polvo fino sin dañar porcelanatos',
        s2_l2: 'Limpieza profunda pre y post-mudanza',
        s2_l3: 'Hidrolavado de techos coloniales, muros de piedra, decks y veredas',
        s3_badge: 'Áreas Verdes',
        s3_t: 'Jardinería y Áreas Exteriores',
        s3_l1: 'Corte de césped, bordes y poda de árboles y arbustos',
        s3_l2: 'Desmalezado pesado y limpieza de terrenos y lotes cerrados',
        s3_l3: 'Abono y control preventivo de plagas (hormigas <em>ysaú</em> y termitas)',
        s4_badge: 'Agua Cristalina',
        s4_t: 'Mantenimiento Completo de Piscinas',
        s4_l1: 'Aspirado, filtrado y cepillado semanal de bordes',
        s4_l2: 'Control químico riguroso (pH, cloro, alcalinidad y alguicida)',
        s4_l3: 'Mantenimiento preventivo de bomba, filtro y sala de máquinas',
        s5_badge: 'Exclusivo Quintas',
        s5_t: 'Casero y "Casa Lista"',
        s5_l1: 'Inspección semanal, apertura para ventilación y control post-lluvia',
        s5_l2: '<strong>Preparación Pre-Llegada:</strong> Encendemos heladera, aire acondicionado y luces antes de que llegue su familia el viernes',
        s5_l3: 'Reporte semanal con fotos enviado por WhatsApp',
        s6_badge: 'Confort y Técnica',
        s6_t: 'Instalaciones Técnicas y Confort',
        s6_l1: 'Instalación y mantenimiento de Aire Acondicionado Split',
        s6_l2: 'Mantenimiento de bombas de pozo artesiano y riego',
        s6_l3: 'Cámaras Wi-Fi para monitoreo remoto, reflectores solares y barniz en decks',
        plans_kicker: 'Transparencia y Previsibilidad',
        plans_title: '5 Planes y Combos a Medida',
        plans_desc: 'Elija entre nuestras suscripciones mensuales de mantenimiento continuo o combos cerrados para obras y revitalización. Valores de referencia para terrenos hasta 1.000 m².',
        plans_sub_heading: 'Suscripciones Mensuales Recurrentes (Tranquilidad Todo el Año)',
        per_month: '/ mes (terrenos hasta 1.000 m²)',
        closed_package: 'paquete cerrado',
        badge_popular: '★ Más Elegido',
        pl1_tag: 'Plan 01 • Esencial',
        pl1_scope: 'Piscina + Jardín',
        pl1_name: 'Piscina y Jardín',
        pl1_desc: 'Ideal para residentes fijos que desean su área exterior siempre limpia y saludable.',
        pl1_f1: '<strong>4 visitas mensuales</strong> de piscina (1 vez por semana)',
        pl1_f2: 'Control químico completo + aspirado',
        pl1_f3: '<strong>2 cortes de césped</strong> y bordes por mes',
        pl1_f4: 'Poda ligera de mantenimiento de arbustos',
        btn_choose_plan1: 'Contratar Plan 1',
        pl2_tag: 'Plan 02 • Completo',
        pl2_scope: 'Piscina + Jardín + Casero',
        pl2_name: 'Quinta Protegida',
        pl2_desc: 'Perfecto para quienes viven en Asunción o en el exterior y usan su quinta los fines de semana.',
        pl2_f1: '<strong>Todo lo del Plan 1</strong> (Piscina semanal + Jardín quincenal)',
        pl2_f2: '<strong>Casero Semanal:</strong> Apertura de la casa para ventilar',
        pl2_f3: 'Revisión de techo, canaletas y bomba de pozo',
        pl2_f4: 'Control preventivo contra hormigas <em>ysaú</em>',
        pl2_f5: '<strong>Reporte semanal con fotos</strong> por WhatsApp',
        btn_choose_plan2: 'Contratar Plan 2',
        pl3_tag: 'Plan 03 • VIP',
        pl3_scope: 'Gestión Total + Limpieza',
        pl3_name: 'Fin de Semana VIP',
        pl3_desc: 'Estándar hotelería: usted llega el viernes y la casa está limpia, fresca y lista.',
        pl3_f1: '<strong>Todo lo del Plan 2</strong> (Piscina + Jardín + Casero)',
        pl3_f2: '<strong>Limpieza ligera pre-llegada</strong> cada jueves o viernes',
        pl3_f3: 'Climatización y heladera encendidas horas antes',
        pl3_f4: '<strong>1 visita mensual de mantenimiento rápido</strong> incluida (reparaciones eléctricas/plomería)',
        btn_choose_plan3: 'Contratar Plan 3',
        combos_heading: 'Combos Cerrados de Alto Impacto (Post-Obra y Revitalización)',
        cb4_tag: 'Combo 04 • Post-Obra',
        cb4_scope: 'Limpieza Fina + Instalaciones',
        cb4_name: 'Paquete "Llave en Mano"',
        cb4_desc: 'Ideal para casas recién construidas o pre-mudanza (hasta 150 m²).',
        cb4_f1: 'Limpieza post-obra fina completa',
        cb4_f2: 'Hidrolavado de veredas exteriores',
        cb4_f3: '1 jornada de instalador (cortinas, TV, espejos, luminarias)',
        cb4_f4: 'Instalación de hasta 2 cámaras Wi-Fi',
        btn_choose_cb4: 'Solicitar Combo 4',
        cb5_tag: 'Combo 05 • Transformación',
        cb5_scope: 'Pintura + Jardín + Piscina + Clima',
        cb5_name: 'Revitalización Total de Quinta',
        cb5_desc: 'Perfecto para pre-temporada de verano o puesta en valor para venta.',
        cb5_f1: 'Hidrolavado de techo y muros',
        cb5_f2: 'Pintura exterior de fachada/muros (hasta 120 m²)',
        cb5_f3: 'Poda pesada, abono y tratamiento de choque en piscina',
        cb5_f4: 'Mantenimiento de hasta 3 equipos de Aire Acondicionado',
        btn_choose_cb5: 'Solicitar Combo 5',
        plans_footnote: '* Para quintas con terrenos superiores a 1.000 m² (2.500 m² a 5.000 m²), aplicamos un adicional proporcional de $30 a $60 USD/mes por desmalezado extra. Consulte condiciones con IVA incluido.',
        how_kicker: 'Proceso Simple y Profesional',
        how_title: 'Cómo funciona nuestro servicio',
        step1_t: 'Inspección y Presupuesto Claro',
        step1_d: 'Nos escribe por WhatsApp, agendamos una visita técnica en Hugua Hú o zona y enviamos una propuesta detallada por escrito, sin sorpresas.',
        step2_t: 'Ejecución Supervisada',
        step2_d: 'Nuestro equipo uniformado o especialistas acreditados realizan el trabajo con equipos profesionales y rigurosa supervisión de calidad.',
        step3_t: 'Entrega y Reporte Fotográfico',
        step3_d: 'Entregamos todo limpio, enviamos las fotos del resultado por WhatsApp y emitimos su Factura Legal con garantía formal.',
        form_kicker: 'Atención Bilingüe (ES / PT)',
        form_title: 'Solicite su Visita o Presupuesto Ahora',
        form_desc: 'Complete los datos al lado para generar su pedido formateado e iniciar la atención inmediata por WhatsApp con el equipo de <strong class="text-amber-300">A Rocha Gestión y Servicios</strong>.',
        info1_t: 'Base y Área de Cobertura',
        info1_d: 'Sede en Hugua Hú • Atención en Atyrá, Altos, Caacupé, Tobatí y San Bernardino.',
        info2_t: 'Horario de Atención',
        info2_d: 'Lunes a Sábado: 07:30 a 18:00 (Guardia de emergencia para suscriptores).',
        info3_t: 'Garantía y Formalidad',
        info3_d: 'Emisión de Factura Legal (IVA) y contrato transparente para planes mensuales.',
        form_fast: 'Tiempo promedio de respuesta por WhatsApp: <strong class="text-white">menos de 15 minutos</strong>.',
        lbl_name: 'Su Nombre *',
        lbl_city: 'Ciudad / Zona de la Propiedad *',
        opt_other_city: 'Tobatí / Otra en Cordillera',
        lbl_plan: 'Plan o Servicio Deseado *',
        opt_p1: 'Plan 1: Piscina y Jardín ($110–$140/mes)',
        opt_p2: 'Plan 2: Quinta Protegida ($170–$220/mes) ★',
        opt_p3: 'Plan 3: Fin de Semana VIP ($280–$360/mes)',
        opt_c4: 'Combo 4: Paquete Llave en Mano ($420–$580)',
        opt_c5: 'Combo 5: Revitalización Total ($850–$1.250)',
        opt_single: 'Servicio Puntual (Reforma / Pintura / Mantenimiento)',
        opt_post: 'Limpieza Post-Obra Puntual',
        lbl_size: 'Tamaño Aproximado del Terreno',
        opt_s1: 'Hasta 1.000 m² (Estándar)',
        opt_s2: '1.000 m² a 2.500 m²',
        opt_s3: '2.500 m² a 5.000 m² (Quinta Mediana)',
        opt_s4: 'Más de 5.000 m² (Quinta Grande)',
        lbl_notes: 'Detalles de lo que necesita (Opcional)',
        btn_submit: 'Enviar Pedido por WhatsApp Ahora',
        footer_brand: 'A ROCHA GESTIÓN Y SERVICIOS',
        footer_copy: '© 2026 A Rocha Gestión y Servicios. Todos los derechos reservados. • Factura Legal y Garantía Técnica.',
        modal_title: 'Resumen Listo para Enviar',
        modal_btn_wa: 'Abrir WhatsApp',
        modal_btn_close: 'Cerrar'
      }
    };

    function setLanguage(lang) {
      currentLang = lang;
      document.documentElement.lang = lang === 'pt' ? 'pt-BR' : 'es-PY';

      const btnPt = document.getElementById('btn-pt');
      const btnEs = document.getElementById('btn-es');

      if (lang === 'pt') {
        btnPt.className = 'px-2.5 py-1.5 rounded-lg text-xs font-extrabold transition bg-amber-400 text-slate-950';
        btnEs.className = 'px-2.5 py-1.5 rounded-lg text-xs font-extrabold transition text-white hover:text-amber-300';
        document.getElementById('clientName').placeholder = 'Ex: Carlos Silva';
        document.getElementById('clientNotes').placeholder = 'Ex: Tenho uma quinta em Hugua Hú com piscina de 8x4m, preciso de manutenção semanal e pintura do muro...';
        document.getElementById('floatingWaBtn').href = 'https://wa.me/595981000000?text=Ol%C3%A1!%20Gostaria%20de%20um%20or%C3%A7amento%20da%20A%20Rocha%20Gest%C3%A3o%20e%20Servi%C3%A7os.';
      } else {
        btnEs.className = 'px-2.5 py-1.5 rounded-lg text-xs font-extrabold transition bg-amber-400 text-slate-950';
        btnPt.className = 'px-2.5 py-1.5 rounded-lg text-xs font-extrabold transition text-white hover:text-amber-300';
        document.getElementById('clientName').placeholder = 'Ej: Carlos Silva';
        document.getElementById('clientNotes').placeholder = 'Ej: Tengo una quinta en Hugua Hú con piscina de 8x4m, necesito mantenimiento semanal y pintura del muro...';
        document.getElementById('floatingWaBtn').href = 'https://wa.me/595981000000?text=%C2%A1Hola!%20Quisiera%20un%20presupuesto%20de%20A%20Rocha%20Gesti%C3%B3n%20y%20Servicios.';
      }

      document.querySelectorAll('[data-i18n]').forEach(el => {
        const key = el.getAttribute('data-i18n');
        if (translations[lang] && translations[lang][key]) {
          el.innerHTML = translations[lang][key];
        }
      });
    }
  </script>
</body>
</html>
