--- 
layout: default 
title: Projects 
permalink: /projects/ 
--- 

<div class="zf-note">
  <div class="zf-note-dot" aria-hidden="true"></div>
  <div class="zf-note-text">
    <strong>Note:</strong> Additional past projects are still being documented and will be added soon
  </div>
</div>

<style>
/* Portfolio WIP note — themed + subtle animation */
.zf-note{
  display:flex;
  align-items:center;
  gap:.75rem;
  padding: .95rem 1.05rem;
  margin: 1.0rem 0 1.4rem 0;
  border-radius: 18px;
  border: 1px solid rgba(86,240,255,.38);
  background: linear-gradient(135deg, rgba(86,240,255,.12), rgba(139,92,246,.10));
  box-shadow:
    0 0 20px rgba(86,240,255,.18),
    0 0 12px rgba(139,92,246,.14);
  color: rgba(234,240,255,.92);
  position: relative;
  overflow: hidden;
}

.zf-note-dot{
  width: 10px;
  height: 10px;
  border-radius: 999px;
  background: rgba(86,240,255,.95);
  box-shadow: 0 0 14px rgba(86,240,255,.65);
  flex: 0 0 auto;
  animation: zfNotePulse 1.9s ease-in-out infinite;
}

.zf-note-text{
  line-height: 1.25;
  font-size: .98rem;
}

/* soft moving sheen */
.zf-note::after{
  content:"";
  position:absolute;
  inset: -40% -30%;
  background: linear-gradient(90deg,
    rgba(255,255,255,0) 0%,
    rgba(255,255,255,.08) 45%,
    rgba(255,255,255,0) 70%);
  transform: rotate(12deg) translateX(-40%);
  animation: zfNoteSheen 3.8s ease-in-out infinite;
  pointer-events:none;
}

@keyframes zfNotePulse{
  0%, 100% { transform: scale(1); opacity: .85; }
  50%      { transform: scale(1.25); opacity: 1; }
}

@keyframes zfNoteSheen{
  0%   { transform: rotate(12deg) translateX(-55%); opacity: .0; }
  15%  { opacity: .9; }
  40%  { opacity: .0; }
  100% { transform: rotate(12deg) translateX(55%); opacity: .0; }
}

/* Mobile spacing */
@media (max-width: 900px){
  .zf-note{ margin-top: .8rem; }
  .zf-note-text{ font-size: .95rem; }
}
</style>


## Featured Engineering Projects 

<div class="gallery-container w-100"> 
  <div class="project-gallery d-flex flex-wrap justify-content-start align-items-start gap-4 w-100"> 
    {% assign featured_projects = site.projects | where: "category", "featured" %} 
    {% for p in featured_projects %} 
      <a class="gallery-item text-decoration-none" href="{{ p.url | relative_url }}" style="display:block; width: 460px;"> 
        
        <!-- image box --> 
        <div style="height: 240px; display:flex; align-items:center; justify-content:center;"> 
          <img src="{{ p.image | relative_url }}" alt="{{ p.imagealt | default: p.title }}" style="max-height: 240px; max-width: 100%; height:auto; width:auto; object-fit: contain; display:block;" > 
        </div> 

        <!-- title --> 
        <p class="mb-0 text-break" style="margin-top: 6px; text-align:center;"> 
          {{ p.title }} 
        </p> 

      </a> 
    {% endfor %} 
  </div> 
</div> 

## Course Projects 

<div class="gallery-container w-100"> 
  <div class="project-gallery d-flex flex-wrap justify-content-start align-items-start gap-4 w-100"> 
    {% assign class_projects = site.projects | where: "category", "class" %} 
    {% for p in class_projects %} 
      <a class="gallery-item text-decoration-none" href="{{ p.url | relative_url }}" style="display:block; width: 460px;"> 
        
        <!-- image box --> 
        <div style="height: 240px; display:flex; align-items:center; justify-content:center;"> 
          <img src="{{ p.image | relative_url }}" alt="{{ p.imagealt | default: p.title }}" style="max-height: 240px; max-width: 100%; height:auto; width:auto; object-fit: contain; display:block;" > 
        </div> 

        <!-- title --> 
        <p class="mb-0 text-break" style="margin-top: 6px; text-align:center;"> 
          {{ p.title }} 
        </p> 

      </a> 
    {% endfor %} 
  </div> 
</div> 
