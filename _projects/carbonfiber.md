---
layout: default
title: "Streamlining Carbon Fiber Manufacturing"
description: CEV Carbon Fiber
category: featured
image: /assets/images/2024chassis.png
---
# Introduction 
When I first joined the team, I noticed that although our composite layups were producing solid results, many steps in the mold preparation process were unnecessarily time-consuming, tedious, or inefficient. I took initiative to analyze the workflow, identify bottlenecks, and implement process improvements to reduce labor time while maintaining—or improving—surface quality and part release performance.

# Streamlining Mold Preparation Process

Once a CNC-machined mold was assembled, our standard workflow involved repairing surface defects with Bondo, hand-sanding up to 400 grit (to avoid the risk of oversanding with power tools), and then spraying Duratec surface primer to achieve a mirror finish prior to layup. After researching industry practices, I found that many groups successfully applied Duratec over lower grit finishes. I tested this by spraying Duratec on a mold sanded only to 180 grit and found that it produced better adhesion and a more uniform primer layer. This change was adopted into our standard process and saves up to six hours of hand sanding per mold, depending on size.
The longest and most labor-intensive step in our workflow was wet sanding the cured Duratec surface up to 2000 grit. Previously, we sanded in a single direction per grit and fully dried the mold between stages to visually confirm scratch orientation before progressing. This approach was slow, wasteful, and required unnecessary sanding beyond what was technically required.

To improve this, I implemented the use of a dry guide coat—a fine powder that settles into the scratches from the previous grit and disappears once those scratches are removed. This eliminated the need to dry the mold between grits, removed the constraint of sanding in only one direction, and prevented oversanding once the surface was already ready to advance. In practice, this reduced sanding time by over 50% while improving consistency.

I also introduced the use of pneumatic sanding tools at higher grits. While power sanding had previously been avoided due to the risk of removing too much material, the guide coat provided clear visual feedback that mitigated this concern. Through testing, I found that pneumatic sanding was unreliable below ~800 grit due to tool size and uneven removal near partially finished regions. As a result, we now hand-sand from 320–600 grit and transition to pneumatic sanding from 800 grit onward, significantly accelerating the process while maintaining surface accuracy and finish quality.

Finally, I investigated whether we could stop sanding at a lower grit while still achieving acceptable layup release. Since the tactile difference between 1000- and 2000-grit finishes is minimal, I performed a trial layup on a mold sanded only to 1000 grit and followed by wool buffing with a heavy-cut compound and foam buffing with a fine polish. However, the part exhibited poor release and excessive adhesion to the mold, indicating that the surface roughness was still too high. Based on this result, we retained sanding to 2000 grit as a necessary step for reliable release performance.

# Wet Layup 

Within Cornell Electric Vehicles (CEV), we use wet layup manufacturing for smaller, non-structural composite components. While wet layups generally produce reduced mechanical performance compared to our vacuum infusion parts, they are well-suited for low-load components and offer greater flexibility for complex geometries and large molds. Many of our “small” parts are still physically large, so we select an extra-slow-curing epoxy system to provide sufficient working time during layup. A representative application of this process is the vehicle side panels, which experience minimal structural loading.

After sanding the mold surface to 2000 grit, I oversee final surface preparation by polishing the mold and applying multiple coats of sealer and release agent to ensure reliable demolding and prevent adhesion between the carbon fiber laminate and the tool surface. This process typically involves approximately eight coats of sealer followed by six coats of release agent, requiring several hours to complete but critical for surface quality and part release.

Once surface preparation is complete, the layup process begins. Because wet layup resin begins curing immediately after mixing, minimizing layup time is essential. If individual resin layers cure at significantly different times, the laminate can develop weak interlaminar bonding and reduced mechanical integrity. To avoid this, my goal is to ensure that the entire laminate cures as uniformly as possible, producing a stronger, more cohesive composite structure.

To support this, I implemented a standardized pre-cutting workflow in which all reinforcement plies are cut and staged prior to resin mixing. This eliminates time spent trimming fabric during layup and allows the team to focus exclusively on resin application and ply placement. For the side panel layup, the laminate schedule consists of two initial carbon fiber plies at 0° and 45°, followed by a Soric lightweight core layer for thickness and stiffness, then a symmetric 45° and 0° outer skin sequence.
After the reinforcement and core layers are placed, we apply a peel ply layer to promote a clean surface finish and simplify secondary bonding operations. Next, I introduced the use of an unperforated release film—an addition to our previous wet layup process. This layer prevents excess resin from being drawn through the peel ply into the breather, ensuring the laminate does not become resin-starved and that the majority of the resin remains within the fiber architecture during cure. A breather layer is then applied to provide an air path for uniform vacuum distribution and to prevent localized pressure gradients across the laminate.

Finally, the entire mold is fully vacuum-sealed and placed under vacuum for the duration of the cure. Although vacuum consolidation is not strictly required for wet layups, applying vacuum significantly improves laminate quality by compacting the fiber stack, removing entrapped air, reducing void content, improving fiber-to-resin contact, and promoting more uniform thickness and surface finish. Vacuum pressure also helps minimize the risk of delamination and enhances overall mechanical performance. After the resin has fully cured, the part is carefully demolded and prepared for trimming and post-processing.

# Vacuum Infusion 

For primary structural components such as the vehicle baseplate and bulkheads, I lead the manufacturing process using vacuum infusion to achieve high fiber volume fraction, low void content, and consistent mechanical performance. These components carry the majority of the vehicle’s weight and global structural loads, making laminate quality and repeatability critical.

We use a one-sided vacuum infusion process with INF-114 epoxy resin cured at room temperature. The laminate schedule consists of a symmetric [0° / 45° / 90°] layup on the mold surface, followed by a Divinycell structural foam core and a mirrored [0° / 45° / 90°] outer skin. To ensure uniform resin flow through the thick sandwich structure, I perforated the Divinycell core and machined internal flow channels throughout the core thickness. This allows resin to fully wet the lower skin, penetrate the core, and saturate the upper laminate without creating dry regions or flow blockages.

Prior to infusion, all reinforcement plies and core layers are pre-cut and staged to minimize handling time and ensure accurate fiber orientation and alignment. After stacking the dry laminate, I install peel ply and green flow media to promote even in-plane resin distribution, followed by spiral wrap inlet lines and strategically placed resin distribution lines to control the flow front and reduce the risk of race-tracking. A dedicated catch pot is integrated into the system to protect the vacuum pump from excess resin during infusion.

Because of the large mold size, full vacuum is not achievable; however, I tune the vacuum level as close to full vacuum as possible to maximize compaction pressure and minimize void formation. During infusion, vacuum consolidation draws resin uniformly through the laminate, removing entrapped air, improving fiber wet-out, and producing a dense, well-consolidated sandwich panel. Compared to wet layup, this process significantly improves fiber-to-resin ratio, thickness uniformity, and interlaminar bonding, resulting in stronger, lighter, and more repeatable structural components.

After the resin has fully infused and cured at room temperature, the part is demolded and prepared for trimming, machining, and final integration into the vehicle chassis.

