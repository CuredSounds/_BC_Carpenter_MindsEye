# _BC_Carpenter_MindsEye

App that takes user photos and text prompts to visualize woodworking projects before committing.

## Software Project Summary

### The Goal
Build a custom, lightweight web application that takes a hand-drawn architectural sketch (structural layout) and a raw photo of wood (texture reference), then uses generative AI to blend them into a photorealistic 3D rendering.

### The Tech Stack
- **Frontend:** React (JavaScript) with drag-and-drop file uploading.
- **Backend:** Python for orchestration and API handling.
- **Rendering pipeline:** ComfyUI (ControlNet + IP-Adapter).
- **GPU hosting:** Serverless GPU API providers such as RunPod or Replicate.

### The Workflow
1. User uploads a structural sketch and slab photo.
2. User optionally adds a text modifier prompt.
3. Backend sends all inputs to a cloud-hosted container running the image-to-image pipeline.
4. Pipeline returns a high-fidelity render to the web dashboard.

## Launch Prompt for a New Chat

Copy and paste this into a new chat window:

```text
I want to build a custom, lightweight web application designed for woodworkers and builders to visualize architectural projects.

The software needs to take two image inputs from a user:
1. A hand-drawn structural layout sketch (acting as the geometric frame reference).
2. A smartphone photo of raw, custom-milled wood slabs (acting as the texture/style reference).

It should combine these images using a text prompt to output a photorealistic 3D architectural render.

I want to use Python for the backend orchestration, React for a simple frontend drag-and-drop user interface, and an open-source tool like ComfyUI (utilizing ControlNet for the sketch lines and IP-Adapter for the wood texture) hosted via a serverless GPU cloud API (like Replicate or RunPod) so I don't have to run massive AI models on my local computer.

Please adopt the persona of a senior software engineer and AI architect. Give me my very first actionable steps to prototype this application, starting with how to set up the visual node workflow in ComfyUI, and how to export that workflow as an API-accessible script.
```
