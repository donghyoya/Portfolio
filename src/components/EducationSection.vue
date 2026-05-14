<template>
  <section id="education">
    <div class="container">
      <div><h2 class="section-title"><img src="data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAAOEAAADhCAMAAAAJbSJIAAAAb1BMVEX///8AAAC9vb2zs7Pn5+eIiIhjY2NcXFxKSkra2tqMjIxGRka3t7coKCijo6OZmZng4OD19fVtbW3w8PBRUVHJycmgoKBWVlbT09Pc3NwlJSUyMjKtra2Tk5MUFBQ4ODiAgIB3d3cTExMbGxtAQEAdSXyQAAAEfklEQVR4nO3a63aiMABGUYsoihWKiFJFxeL7P+NQTSBAUDBepmud/WNGMQY+IRdCBwMAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAA/5Xg7N1H8QS7Uc61BsOP/X6fzcev2q8dJ6PjYuysx4tj6kdfT9vR9ONi6ooXul0F8dnjTnCUnj5qtovoYdVXyITfMqGu0FF8Nmyrxb6uVjqZ1+NdZL5hmHjn14RlwsHo8r+j+6YjCq1bap7oj7iwUQt/ba+UjI0SLhv1+c2EunYYHEShpKXm2Y2E6oURXy/Zepl04TSq65jwS5Zvayk9EoY/N4qanMW7E/qy/MI8oVtudEb+Ksl5vrvYFFuX70hY/uxT44R7scWtdT9BIsvW+6UXJFR+9pNxQrHBa1Yi24LBoNFMOOyS8Fv9xuhawuXO1RpZjYTj5tjqiY8MGqJI6ITqOHUzYVAdvDQ/fpFw1+Eg5Omeu5FyOYaxV1wH4b35ioTVDDcT1scYXURxdGl4e8QfKlVl29lyuVxPDhtlY1tv9rSEzUtbc6HeaoebqxVWZAan8J6EQXEG96PiINaN3q7PiB80Jx5qwG+DgPqEcoqhTfhdTrD8wbg8jvrcpk/C/G6mvdzY5AwWCX+287MsirP5XDYBXUK/3HU+DgfKfPL0aZBwYLv6UguzWWmzBXif6jE0Eg6z8tPD74bqhGunjP49E+bGzTJbw3j9EgbTyqV0ulw8Ye2mbi0Htf4JF6KGZLXyRFqT6VrvhHZLEnlgkuwWRMKx9anXnOyJitLf17s3JAwztVyq1JGoHxSNsceILxzfnLAS0apUYpd3u+XA2DFh4EmJqGWZ5K/FcW0T+enq3qmpqCmbzM5OUzv/V97c1noaW/YqzQmkJfrUWblJJNzP9TaHSztWf9Gr5neuCImE1WmRnNHX+9LLODnT/prW+QwoS1Y3e5pLNVbXhAezhB3nNHmLc1qvlu/dTF01+psJB0n3W9E/mrCH/zVhEMbhYxI2lnf1CdVltn1WXZKqvG9bteyYcBJZ1tAfHZ381nb1mITubHLVTEyo7a8L+8sazSpj7sdmuYps+fm9i+uaO7P1YxL2FHjaJeQfx7r93at0957vSOhpjkOeSbNnF7qEcdt4+DTB9UcAqUnduoS+NmHeUjuJepSV935Xb/ENI+oSprqE4Y2DKJV98W2Xg1gpWzbL8eKXM9krWw0u1HV1j5ux60217bB283SFfetBSyNh8daPlQfOQRgV60AG7cQeitu1/JIp5isvTigvD82IV6yS3J9Q68UJ5QK67iHaTi34ZxMG4s2hOemNRWPMXpCwe09j9+5piilsGqkrh7ZVLJCkL0g4iIbd/HZ7VseyYrSIlMybiXNM03SxPqkzOIOna90TPpM6XOiYztwaXj9rS1rDfRhP23TeMC+1F60B3Sf8TVZwPE8r/EF62Yf2r00ezfYPmnjO8Ll/cxYmZ49u520CyzvOxEOT/XbtJqbPLAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAABz/wAFjEI3yFpj/QAAAABJRU5ErkJggg==" style="max-width: 100% !important; height: auto !important; border-radius: 4px !important; display: inline-block !important; vertical-align: middle !important;"><br></h2></div>
      <h2 class="section-title">학력</h2>
      <div class="edu-card">
        <div class="edu-icon">🎓</div>
        <div class="edu-info">
          <h3>서울대학교</h3>
          <p class="major">소프트웨어학부 소프트웨어학과</p>
          <p class="detail">Seoul, Korea</p>
        </div>
      </div>
    </div>
  </section>
</template>

<style scoped>
.edu-card {
  display: flex;
  align-items: center;
  gap: 24px;
  background: var(--bg-card);
  border: 1px solid var(--border);
  border-radius: var(--radius);
  padding: 32px;
  max-width: 540px;
  transition: border-color 0.2s, transform 0.2s;
}

.edu-card:hover {
  border-color: var(--accent);
  transform: translateY(-4px);
}

.edu-icon {
  font-size: 3rem;
  flex-shrink: 0;
}

.edu-info h3 {
  font-size: 1.4rem;
  font-weight: 700;
  margin-bottom: 6px;
}

.major {
  color: var(--accent);
  font-size: 0.95rem;
  font-weight: 500;
  margin-bottom: 4px;
}

.detail {
  color: var(--text-muted);
  font-size: 0.875rem;
}
</style>
