# POV Product Review Videos

## Lock the template before you generate

- Use this template when the user asks for a POV product review video or asks to reuse the saved POV review style with a new product.

- Confirm the product, the background and the voiceover details before you generate anything.

- Ask once about voice gender, language, tone and spoken content when those details are unknown, then use the answer for every later video in the same batch.

- Keep the fixed format as 20 seconds, vertical 9 to 16, and POV from the viewer own hands unless the user changes one of those choices.

- Follow the shot rhythm of a slow to medium pace with each angle held for 2 to 3 seconds.

- Follow the shot order of 0 to 5 seconds for the opening hand held shot, 5 to 12 seconds for close detail, 12 to 17 seconds for context and 17 to 20 seconds for the closing centered shot.

## Keep the product identical and physically true

- Use the original product photo as the reference for every segment and keep its design, details and colour unchanged.

- Change the background before you generate the video and prefer a clean luxurious store setting when the user has not chosen another setting.

- Keep the background clean with no added logo, text or other brand that could cause a TikTok problem.

- When the user sends a video instead of a still photo, ask for a clear still photo rather than using a blurry extracted frame as the reference.

- Show only actions that work in real life and keep every fit, contact and movement physically true.

- For a battery charger, show the battery fitted snugly with its end touching the contact above and no gap, and never show a press down move that opens a gap.

- Drop an action you cannot show correctly and show the product already fitted or in use instead.

- Keep the product size true to life against the hand, the table and nearby objects so a heavy pack looks large and heavy in the frame.

## Build 20 seconds in verified segments — scenes must continue, never restart

- Build the 20 seconds as two 10 second segments and join them, because one generation pass gives at most 10 seconds.

- Write ONE master dialogue script first, split across the scenes, one unique line per scene, no line repeated. Scene 2 must not re-introduce the product and must not repeat scene 1's words.

- Generate scenes SEQUENTIALLY, never in parallel and never as independent standalone videos. Finish scene 1, then generate scene 2 by resuming scene 1's snapshot, with dual reference: the final frame of scene 1 plus the original product photo. Scene 2 must start mid-action, continuing the exact dangling action scene 1 ended with, and speak only its own dialogue line.

- Reuse the same original photo as the reference for the second segment so the product does not change after the first 10 seconds.

- Never reuse scene 1's full prompt for scene 2. Scene 2's prompt must state it is a continuation, not a new video, with no re-introduction and no repeated dialogue.

- Join with a 0.5 second crossfade and audio acrossfade, never with a plain concat copy, which makes the scenes look like separate videos.

- Check the returned duration and orientation for each segment before you join them or report the video as complete.

- Check the generation task status before you retry a failed segment, because a failed call may already have completed.

- If a segment fails, report the video as incomplete at 10 seconds, name the failed segment and offer the next step instead of claiming a 20 second video.

- Work through a batch product by product and keep a clear list of completed videos, incomplete videos and videos not yet started.

## Report only what you verified

- Report the length, the orientation and the presence of audio only from the returned file details.

- Never claim that a video has no voiceover or only music, and never describe sounds or pictures you did not watch or listen to.

- Say plainly what you checked and what you could not check when you deliver a video.

- When the user corrects a detail, name the correction, apply it to the current video and carry it into the rest of the batch.

- Before delivering a multi-scene video, check continuity: extract frames at each scene junction and confirm the last frame of one scene and the first frame of the next show the same ongoing action, and that no scene re-opens with the same introduction or dialogue as scene 1.

## Available connectors

- [Runway](/opt/hatch/connectors/runway_mcp/CONNECTOR.md) for generating and editing video, images and speech.

- Use `muse.connector_search` to find other connectors and `muse.skill_search` to find related skills.

- If nothing here fits, look on the web for a maintained API or MCP server and set it up with [Custom Connectors and MCPs](/opt/muse/skills/custom-connector-setup/SKILL.md), or build a custom connector.

## Alternatives for better results

- Ask for one clear product photo per video when the user sends several products at once, so each video has its own reference.

- Offer a still image test of the new background before you generate a full batch when the background is new.

- Offer to drop a risky handling shot and use a fitted product shot when a physical action keeps failing.
