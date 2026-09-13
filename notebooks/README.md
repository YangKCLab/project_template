This folder stores your experiments.

Create a dated folder for each experiment, such as `2026-01-15_first_data_exploration` or `2026-02-03_model_visualization`. Dated folders make experiments easy to find later and keep the folder organized when several people work on the project.

Use literate and interactive tools such as Jupyter Lab (`uv run jupyter lab`). Don't overcomplicate.
If the project is simple, a series of notebooks may be all you need.
If the project involves complex data manipulation and many computation steps, keep each experiment small and focused. Move what works into `libs/` and `workflow/` so the whole pipeline can be tested, automated, and modularized.
