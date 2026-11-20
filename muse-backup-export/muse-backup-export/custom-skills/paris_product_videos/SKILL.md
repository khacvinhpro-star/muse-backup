# Paris Product Videos

## Research and lock the product, host and warehouse before you generate

- Study the product photo and the product link before you generate anything, including shape, colour, material, small details, size, proportion and use.

- Use only information you verified from the photo and the link, never guess or invent a detail, and say plainly what you could not verify instead of filling it in.

- Use the original product photo as the reference for every scene and keep its design, details, colour, label and packaging text unchanged.

- When the reference photo shows a KOC or model, focus only on the product and use a different person in the video, never the same person from the original photo.

- Keep the same host in every scene, a young woman in a black uniform with a STAFF name badge, with the same face, hair and outfit throughout.

- Choose the warehouse or factory that matches the product industry, such as a detergent plant for detergent, a shoe factory for shoes, a garment factory for clothing, a home appliance plant for appliances, a food plant for food and a cosmetics plant for cosmetics.

- Never reuse the detergent warehouse as the default for a different product.

- Keep at most two variants of one product together in the frame and keep their left to right order the same in every scene.

## Build 24 seconds in sequential scenes that continue, never restart

- Keep the fixed format as 24 seconds, vertical 9 to 16, 1080 by 1920, with an on-camera host who speaks directly to the camera, never a hand-only POV video.

- Open with the host walking toward the camera while holding the product with both hands, with stacks of identical products behind her, then move to close label shots and macro shots of the cap, handle and label details.

- Show the warehouse yard with a truck being loaded and workers in the background, then the conveyor and packing line, still keeping the product at the centre of the frame.

- Show two real demos in sequence, such as pouring the product correctly and then using it on a real object, and close with the host holding the product at the centre of the frame while speaking to the camera.

- Write one dialogue script first and split it across the scenes, with one unique line per scene of about 100 to 130 characters, and never repeat a line or reintroduce the product in a later scene.

- Generate scenes sequentially, never in parallel, and generate each later scene by resuming the previous scene snapshot, with dual reference to the final frame of the previous scene plus the original product photo.

- Start each later scene in the middle of the dangling action the previous scene ended with, speak only that scene own line, and never reuse the first scene full prompt for a later scene.

- Join scenes with a 0.5 second crossfade and audio acrossfade, never with a plain concat copy, and trim segments when needed so the total stays near 24 seconds.

- Show only actions that work in real life, keep every fit, contact and movement physically true, and drop an action you cannot show correctly and show the product already in use instead.

- Keep the product size true to life against the hand, the table and nearby objects so a large heavy pack looks large and heavy in the frame.

- Do not state a price when the link does not state one clearly, and do not make a health claim or an absolute claim.

## Check continuity and report only what you verified

- Check the returned duration and orientation for each segment before you join them or report the video as complete.

- Before you deliver a multi-scene video, check continuity by looking at the first frame of each scene and confirming no scene reopens with the same introduction or dialogue as scene 1, and that the last frame of one scene and the first frame of the next show the same ongoing action.

- Check that the product, the host, the uniform and the warehouse stay identical across scenes, that paired variants keep their order, and that no added logo, text or other brand appears on screen.

- Report the length, the orientation and the presence of audio only from the returned file details, never claim a sound or picture you did not watch or listen to, and say plainly what you checked and what you could not check.

- Ask once about voice gender, language, tone and spoken content when those details are unknown, then use the answer for every later video in the same batch, and never default to a voice the user has not confirmed.

- Write a caption of one main benefit line, one use line and one soft closing line, with four to five hashtags that name the product and its type, and keep price and absolute claims out of the caption.

## Available connectors

- [Runway](/opt/hatch/connectors/runway_mcp/CONNECTOR.md) for generating and editing video, images and speech.

- Use `muse.connector_search` to find other connectors and `muse.skill_search` to find related skills.

- If nothing here fits, look on the web for a maintained API or MCP server and set it up with [Custom Connectors and MCPs](/opt/muse/skills/custom-connector-setup/SKILL.md), or build a custom connector.

## Alternatives for better results

- Offer a still image test of a new warehouse setting before you generate a full video when the setting is new.

- Ask for one clear product photo per video when the user sends several products at once, so each video has its own reference.

- Offer to drop a risky handling shot and use a fitted product shot when a physical action keeps failing.
