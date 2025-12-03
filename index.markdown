---
layout: page
title: "SwissDataExplorers"
subtitle: "Can the market see the future?"
---

<!-- ======================= -->
<!--  Intro / Hero text      -->
<!-- ======================= -->

<div class="content">
  <p>
    This is our ADA 2025 data story. We explore whether stock markets react
    to innovation events (product launches, keynotes, major announcements)
    in a systematic and predictable way.
  </p>
</div>

<hr>

<!-- ======================= -->
<!--  Why this matters       -->
<!-- ======================= -->

<section class="section">
  <h2 class="title is-3">Why this matters</h2>
  <div class="columns">
    <div class="column">
      <div class="content">
        <p>
          Innovation drives long-term value, but markets don’t always react
          in a clean, textbook way. Sometimes they anticipate, sometimes
          they overreact, and sometimes they completely ignore news that
          looks important on paper.
        </p>
        <p>
          Our goal is to quantify how markets price innovation events, and
          to see whether we can detect consistent reaction patterns across
          companies and event types.
        </p>
      </div>
    </div>
    <div class="column">
      <div class="box">
        <p class="heading">We ask questions like:</p>
        <ul>
          <li>Do “big launches” always yield positive abnormal returns?</li>
          <li>Is the reaction symmetric for good vs. bad surprises?</li>
          <li>Are some companies systematically “overhyped”?</li>
        </ul>
      </div>
    </div>
  </div>
</section>

<!-- ======================= -->
<!--  Key Numbers Section    -->
<!-- ======================= -->

<section class="section">
  <div class="columns is-multiline has-text-centered">
    <div class="column is-one-quarter">
      <div class="box">
        <p class="title is-3">10k+</p>
        <p class="heading">Trading days</p>
      </div>
    </div>
    <div class="column is-one-quarter">
      <div class="box">
        <p class="title is-3">100+</p>
        <p class="heading">Tech companies</p>
      </div>
    </div>
    <div class="column is-one-quarter">
      <div class="box">
        <p class="title is-3">500+</p>
        <p class="heading">Events</p>
      </div>
    </div>
    <div class="column is-one-quarter">
      <div class="box">
        <p class="title is-3">4</p>
        <p class="heading">ML models</p>
      </div>
    </div>
  </div>
</section>

<!-- ======================= -->
<!--  Story Overview         -->
<!-- ======================= -->

<section class="section">
  <h2 class="title is-3">Our main question</h2>
  <div class="content">
    <p>
      When a company announces a major innovation (e.g., a new device, a breakthrough
      product, a strategic shift), does the market:
    </p>
    <ul>
      <li>React instantly on the announcement day?</li>
      <li>Anticipate the news before it happens?</li>
      <li>Underreact and adjust over the next few days?</li>
    </ul>
    <p>
      We combine daily stock prices with a curated set of innovation-related events
      and analyze abnormal returns around each event.
    </p>
  </div>
</section>

<!-- ======================= -->
<!--  Pipeline / Method      -->
<!-- ======================= -->

<section class="section">
  <h2 class="title is-3">From raw data to insight</h2>
  <div class="columns is-multiline">
    <div class="column is-one-quarter">
      <div class="box">
        <p class="heading">Step 1</p>
        <p class="title is-5">Collect</p>
        <p class="content is-small">
          Stock prices (NASDAQ), innovation events (product launches, announcements),
          and market benchmarks.
        </p>
      </div>
    </div>
    <div class="column is-one-quarter">
      <div class="box">
        <p class="heading">Step 2</p>
        <p class="title is-5">Align</p>
        <p class="content is-small">
          Match each event to the corresponding ticker and trading days,
          build event windows.
        </p>
      </div>
    </div>
    <div class="column is-one-quarter">
      <div class="box">
        <p class="heading">Step 3</p>
        <p class="title is-5">Model</p>
        <p class="content is-small">
          Estimate expected returns using market models, compute abnormal returns,
          and feed them to ML models.
        </p>
      </div>
    </div>
    <div class="column is-one-quarter">
      <div class="box">
        <p class="heading">Step 4</p>
        <p class="title is-5">Explain</p>
        <p class="content is-small">
          Visualize how reactions differ by company, event type, and time horizon.
        </p>
      </div>
    </div>
  </div>
</section>

<!-- ======================= -->
<!--  Case studies           -->
<!-- ======================= -->

<section class="section">
  <h2 class="title is-3">Case studies (teaser)</h2>
  <div class="columns">
    <div class="column">
      <div class="card">
        <header class="card-header">
          <p class="card-header-title">
            Example 1 – Big device launch
          </p>
        </header>
        <div class="card-content">
          <div class="content">
            <p>
              Strong positive reaction on day 0, followed by a mild correction.
            </p>
            <ul>
              <li>Company: <strong>Apple-like</strong></li>
              <li>Peak abnormal return: <strong>+2.0%</strong></li>
              <li>Drift over 5 days: <strong>+0.5%</strong></li>
            </ul>
            <p class="is-size-7">
              (In the final version, this card will show a real event from our dataset.)
            </p>
          </div>
        </div>
      </div>
    </div>
    <div class="column">
      <div class="card">
        <header class="card-header">
          <p class="card-header-title">
            Example 2 – Overhyped keynote
          </p>
        </header>
        <div class="card-content">
          <div class="content">
            <p>
              Strong run-up before the event, flat or negative abnormal return on day 0.
            </p>
            <ul>
              <li>Pattern: <strong>anticipation then disappointment</strong></li>
              <li>Pre-event drift: <strong>+3%</strong></li>
              <li>Event-day abnormal: <strong>-1%</strong></li>
            </ul>
          </div>
        </div>
      </div>
    </div>
    <div class="column">
      <div class="card">
        <header class="card-header">
          <p class="card-header-title">
            Example 3 – Under-the-radar update
          </p>
        </header>
        <div class="card-content">
          <div class="content">
            <p>
              No big move on day 0, but slow positive drift over the next week.
            </p>
            <ul>
              <li>Market initially ignores the news</li>
              <li>Post-event drift: <strong>+1.5%</strong></li>
            </ul>
          </div>
        </div>
      </div>
    </div>
  </div>
</section>

<!-- ======================= -->
<!--  How to read the charts -->
<!-- ======================= -->

<section class="section">
  <h2 class="title is-3">How to read our charts</h2>
  <div class="columns">
    <div class="column">
      <div class="box">
        <p class="heading">Event window</p>
        <p class="content is-small">
          We center each chart on day <strong>0</strong>, the event day. Negative
          values on the x-axis are days before the event, positive values are
          days after.
        </p>
      </div>
    </div>
    <div class="column">
      <div class="box">
        <p class="heading">Abnormal returns</p>
        <p class="content is-small">
          Returns are adjusted for overall market movements. A value of
          <strong>+1%</strong> means the stock outperformed our benchmark by 1%
          on that day.
        </p>
      </div>
    </div>
    <div class="column">
      <div class="box">
        <p class="heading">Aggregation</p>
        <p class="content is-small">
          Curves represent averages over many events of the same type
          (e.g. product launches for a given company).
        </p>
      </div>
    </div>
  </div>
</section>

<!-- ======================= -->
<!--  Interactive Chart #1   -->
<!-- ======================= -->

<section class="section">
  <h2 class="title is-3">How does the market react around an event?</h2>
  <div class="content">
    <p>
      Below, you can explore the average abnormal return around a hypothetical
      innovation event. Use the buttons to switch between example companies.
      Later we will plug in our real estimated abnormal returns.
    </p>
  </div>

  <div class="buttons has-addons is-centered">
    <button class="button is-info is-light" data-company="apple">Apple</button>
    <button class="button is-info is-light" data-company="microsoft">Microsoft</button>
    <button class="button is-info is-light" data-company="tesla">Tesla</button>
  </div>

  <div class="box">
    <canvas id="eventReactionChart" style="max-height: 400px;"></canvas>
  </div>
</section>

<!-- ======================= -->
<!--  Interactive Chart #2   -->
<!-- ======================= -->

<section class="section">
  <h2 class="title is-3">Surprise vs. reaction by event type</h2>
  <div class="content">
    <p>
      Here we show a toy example of how <em>innovation surprise</em> (how unexpected
      the event is) could relate to average abnormal returns on the announcement day.
      Use the buttons to switch between different event types.
    </p>
  </div>

  <div class="buttons has-addons is-centered">
    <button class="button is-warning is-light" data-event-type="product">Product launches</button>
    <button class="button is-warning is-light" data-event-type="keynote">Keynotes</button>
    <button class="button is-warning is-light" data-event-type="ma">M&amp;A / strategic deals</button>
  </div>

  <div class="box">
    <canvas id="surpriseChart" style="max-height: 300px;"></canvas>
  </div>
</section>

<!-- ======================= -->
<!--  Team / Links           -->
<!-- ======================= -->

<section class="section">
  <h2 class="title is-3">Team &amp; resources</h2>
  <div class="columns">
    <div class="column is-two-thirds">
      <div class="content">
        <p><strong>Team:</strong> SwissDataExplorers</p>
        <ul>
          <li>Rami – data pipelines &amp; modeling</li>
          <li>… – event curation &amp; labeling</li>
          <li>… – visualization &amp; narrative</li>
        </ul>
        <p>
          Code, notebooks and full report are available on our GitHub repo:
        </p>
        <p>
          <a href="https://github.com/USERNAME/REPO" target="_blank">
            View project on GitHub
          </a>
        </p>
      </div>
    </div>
    <div class="column">
      <div class="box">
        <p class="heading">Deliverables</p>
        <ul class="is-size-7">
          <li>Exploratory notebooks</li>
          <li>Cleaned event &amp; price datasets</li>
          <li>Model comparison (baseline vs ML)</li>
          <li>Final report &amp; slides</li>
        </ul>
      </div>
    </div>
  </div>
</section>

<!-- ======================= -->
<!--  JS & Chart.js          -->
<!-- ======================= -->

<!-- Load Chart.js from CDN -->
<script src="https://cdn.jsdelivr.net/npm/chart.js"></script>

<script>
document.addEventListener("DOMContentLoaded", function () {
  // --- Data for interactive chart #1 (toy data to start with) ---
  const days = [-5, -4, -3, -2, -1, 0, 1, 2, 3, 4, 5];

  const eventData = {
    apple:     [-0.2, 0.1, 0.0, 0.2, 0.3, 1.5, 0.8, 0.3, 0.1, 0.0, -0.1],
    microsoft: [-0.1, 0.0, 0.1, 0.1, 0.2, 0.9, 0.5, 0.2, 0.1, 0.0, 0.0],
    tesla:     [-0.5, 0.0, 0.3, 0.5, 0.8, 2.0, 1.2, 0.6, 0.2, 0.0, -0.2]
  };

  const ctx1 = document.getElementById("eventReactionChart").getContext("2d");

  const eventChart = new Chart(ctx1, {
    type: "line",
    data: {
      labels: days,
      datasets: [
        {
          label: "Average abnormal return (%)",
          data: eventData.apple,
          fill: false
        }
      ]
    },
    options: {
      responsive: true,
      plugins: {
        legend: { display: true },
        title: {
          display: true,
          text: "Abnormal return around event day (day 0)"
        }
      },
      scales: {
        x: {
          title: { display: true, text: "Days relative to event" }
        },
        y: {
          title: { display: true, text: "Abnormal return (%)" }
        }
      }
    }
  });

  // Buttons to switch company on chart #1
  const companyButtons = document.querySelectorAll("[data-company]");
  companyButtons.forEach(function (btn) {
    btn.addEventListener("click", function () {
      const company = this.getAttribute("data-company");
      eventChart.data.datasets[0].data = eventData[company];
      eventChart.update();
    });
  });

  // --- Data for interactive chart #2 (toy data per event type) ---
  const surpriseLevels = ["Low", "Medium", "High"];

  const surpriseData = {
    product:  [0.2, 0.8, 1.5],
    keynote:  [0.1, 0.5, 0.9],
    ma:       [-0.3, 0.4, 1.2]
  };

  const ctx2 = document.getElementById("surpriseChart").getContext("2d");
  const surpriseChart = new Chart(ctx2, {
    type: "bar",
    data: {
      labels: surpriseLevels,
      datasets: [
        {
          label: "Average abnormal return on day 0 (%)",
          data: surpriseData.product
        }
      ]
    },
    options: {
      responsive: true,
      plugins: {
        legend: { display: false },
        title: {
          display: true,
          text: "Event surprise vs. market reaction (toy example)"
        }
      },
      scales: {
        x: {
          title: { display: true, text: "Innovation surprise" }
        },
        y: {
          title: { display: true, text: "Abnormal return (%)" }
        }
      }
    }
  });

  // Buttons to switch event type on chart #2
  const eventTypeButtons = document.querySelectorAll("[data-event-type]");
  eventTypeButtons.forEach(function (btn) {
    btn.addEventListener("click", function () {
      const eventType = this.getAttribute("data-event-type");
      surpriseChart.data.datasets[0].data = surpriseData[eventType];
      surpriseChart.update();
    });
  });
});
</script>
