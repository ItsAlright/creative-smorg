<script>
  const projects = [
    {
      title: "Project One",
      description: "A brief description of your first project",
      technologies: ["SvelteKit", "TypeScript", "Tailwind"],
      imageUrl: "/placeholder-1.jpg",
      link: "https://github.com/yourusername/project-one"
    },
    {
      title: "Project Two",
      description: "Description of your second project",
      technologies: ["React", "Node.js", "MongoDB"],
      imageUrl: "/placeholder-2.jpg",
      link: "https://github.com/yourusername/project-two"
    }
  ];
</script>

<section class="py-16 px-4 bg-gray-50">
  <div class="max-w-6xl mx-auto">
    <h2 class="text-3xl font-bold mb-12 text-center">My Projects</h2>
    <div class="grid grid-cols-1 md:grid-cols-2 gap-8">
      {#each projects as project}
        <div class="bg-white rounded-lg shadow-md overflow-hidden">
          <img src={project.imageUrl} alt={project.title} class="w-full h-48 object-cover"/>
          <div class="p-6">
            <h3 class="text-xl font-semibold mb-2">{project.title}</h3>
            <p class="text-gray-600 mb-4">{project.description}</p>
            <div class="flex flex-wrap gap-2 mb-4">
              {#each project.technologies as tech}
                <span class="px-3 py-1 bg-gray-100 rounded-full text-sm">
                  {tech}
                </span>
              {/each}
            </div>
            <a href={project.link} class="text-blue-600 hover:underline">View Project →</a>
          </div>
        </div>
      {/each}
    </div>
  </div>
</section>