<script>
  import Step from "./Step.svelte";

  let steps = [
    { name: "C Language Quiz", icon: "fa-solid fa-scroll", href: "" },
    { name: "Jump Queen", icon: "fa-solid fa-gamepad", href: "" },
  ];

  let benefits = [
    {
      name: "A Passionate Learner",
      description:
        "I fell in love with coding after taking my first class in university. I love the aspect of continuously learning new things and the ability to be creative with my work. It all started with Python and now I have coded in tons of languages and learned new concepts such as OOP and Agile methodologies.",
    },
    {
      name: "A Strong Problem Solver",
      description:
        "One of my favourite things to do is solve problems, and anyone who has ever attempted to code, knows how many problems you have got to solve. Whether its a layout not displaying how it should or a calculation going awry, I'm always willing to accept the challenge.",
    },
    {
      name: "Team Player",
      description:
        "Growing up I played a number of team sports including football, lacrosse, basketball and rugby and I now coach football as well. From my time around all those sports I learned the importance teamwork. If everyone communicates effectively, is accountable for their own jobs, and trusts eachother, then the team will prosper and achieve their goals.",
    },
  ];
</script>

<main class="flex flex-col flex-1 p-4">
  <section
    id="introPage"
    class="grid grid-cols-1 lg:grid-cols-2 gap-10 py-8
			sm:py-14"
  >
    <div
      class="flex flex-col lg:justify-center text-center lg:text-left
					gap-6 md:gap-8 lg:gap-10"
    >
      <h2 class="font-semibold text-3xl sm:text-4xl md:text-5xl">
        Hi! I'm <span class="poppins text-green-400">Justin</span>
        Pearson <br /> Computer Science
        <span class="poppins text-green-400">Student</span>
      </h2>
      <p class="text-base sm:text-lg md:text-xl">
        My <span class="poppins text-green-400">favourite languages</span> are
        javascript, python and C! Graduating from MacEwan University in
        <span class="poppins text-green-400">April 2024!</span>
      </p>
      <a
        class="greenshadow mx-auto lg:mr-auto lg:ml-0 text-base sm:text-lg md:text-xl
      poppins relative overflow-hidden px-6 py-3 group rounded-full bg-white
      text-slate-950"
        href="www.linkedin.com/in/justin-pearson5252"
        target="_blank"
      >
        <div
          class="absolute top-0 right-full w-full h-full bg-green-400 opacity-20
	    group-hover:translate-x-full z-0 duration-200"
        />
        <h4 class="relative z-9">Get in touch &rarr;</h4>
      </a>
    </div>
    <div class="relative grid place-items-center">
      <img
        src={"images/profile.png"}
        alt="Profile image"
        class="object-cover
		z-[2] max-h-[50vh]"
      />
    </div>
  </section>

  <section id="projects" class="py-20 lg:py-32 flex flex-col gap-24">
    <div class="flex flex-col gap-2 text-center">
      <h6 class="text-lg sm:text-xl md:text-2xl">
        A few of my learning projects.
      </h6>
      <h3 class="font-semibold text-3xl sm:text-4xl md:text-5xl">
        <span class="poppins text-green-400">curious</span> to see my work?
      </h3>
    </div>
    <a
      href="https://github.com/JP5252?tab=repositories"
      target="_blank"
      class="mx-auto px-4 py-2 rounded-md border
	  border-solid border-white flex items-center gap-2 -mb-4 sm:-mb-0 -mt-10
	  hover:border-green-700 duration-200"
    >
      <i class="fa-brands fa-github"></i>
      <p>Check this out!</p>
    </a>
    <div class="grid grid-cols-1 lg:grid-cols-2 gap-12 lg:gap-10">
      <Step step={steps[0]}>
        <p>
          The C language quiz that will test your knowledge on the C programming
          language, this was my <strong class="text-green-400"
            >first React app!</strong
          >
        </p>
      </Step>
      <Step step={steps[1]}>
        <p>
          <strong class="text-green-400">Jump Queen</strong> is a 2D game I am
          currently working on in <strong class="text-green-400">Unity</strong> for
          a class at school, taking inspiration from the game jump king!
        </p>
      </Step>
    </div>
  </section>

  <section
    id="about"
    class="py-20 pt-10 lg:pt-16 flex flex-col gap-16 sm:gap-20
  md:gap-24 relative"
  >
    <div
      class="flex flex-col gap-2 text-center relative before:absolute
  before:top-0 before:left-0 before:w-2/3 before:h-1.5 before:bg-green-700 after:absolute
  after:bottom-0 after:right-0 after:w-2/3 after:h-1.5 after:bg-green-700 py-4"
    >
      <h6 class="text-lg sm:text-xl md:text-2xl">Want to know more?</h6>
      <h3 class="font-semibold text-3xl sm:text-4xl md:text-5xl">
        A bit <span class="poppins text-green-400">about</span> me.
      </h3>
    </div>
    <p class="mx-auto poppins font-semiblod text-xl sm:text-2xl md:text-3xl">
      I am...
    </p>
    <div class="flex flex-col gap-20 w-full mx-auto max-w-[800px]">
      {#each benefits as benefit, index}
        <div class="flex gap-6 sm:gap-8">
          <p
            class="poppins text-4xl sm:text-5xl md:text-6xl text-slate-500
			font-semibold"
          >
            0{index + 1}
          </p>
          <div class="flex flex-col gap-6 sm:gap-8">
            <h3 class="text-2xl sm:text-3xl md:text-4xl">
              {benefit.name}
            </h3>
            <p>{benefit.description}</p>
          </div>
        </div>
      {/each}
    </div>
  </section>
</main>
