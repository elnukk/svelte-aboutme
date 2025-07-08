<script>
  import FloatingShapes from './lib/FloatingShapes.svelte';
  import Header from './lib/Header.svelte';
  import Card from './lib/Card.svelte';
  import Timeline from './lib/Timeline.svelte';
  import Highlights from './lib/Highlights.svelte';

  const timeline = [
    { year: "2022", description: "Became a KWK scholar and did the virtual webdev camp" },
    { year: "2024", description: "One of the finalists for the KWK x Estee Lauder Web Design Challenge" },
    { year: "And again in 2024", description: "Started as a community ambassador and created content for socials" },
  ];

  const funFacts = [
    "I love motorbiking and am currently learning how to drive stickshift to get my driver's license.",
    "I have a solo trip booked for this summer and I'm HYPED.",
    "My name is made up by my mom and I am the only one in the world with my full name."
  ];

  const highlights = [
    { icon: "✈️", title: "Travel", text: "Traveled to Portugal with a friend from college!" },
    { icon: "📚", title: "Projects", text: "Built a web app for helping kids practice reading" },
    { icon: "🎵", title: "Music", text: "Been to 5 concerts this year" }
  ];
</script>

<FloatingShapes />

<div class="container">
  <Header name="Elanu Karakus" tagline="19 yo • Stanford CS • 🇹🇷" />

  <Card title="About Me">
    <p>Hi! I'm Elanu, a 19-year-old CS student at Stanford. What I really like about technology is that it gives you an opportunity to turn your ideas into something tangible. I’m currently interning at a tech nonprofit that is building AI tools for smallholder farmers for sustainable farming practices!</p>
  </Card>

  <Card title="My KWK Journey">
    <Timeline items={timeline} />
  </Card>

  <Card title="Fun Facts">
    {#each funFacts as fact, i}
      <p>{i + 1}) {fact}</p>
    {/each}
  </Card>

  <Card title="Recent Highlights">
    <Highlights {highlights} />
  </Card>
</div>
