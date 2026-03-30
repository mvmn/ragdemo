Code for simple RAG demo

DB init script:

```
CREATE EXTENSION vector;

CREATE TABLE public.embeddings_refined (
	id bigserial NOT NULL,
	article varchar(64) NOT NULL,
	chunk_id varchar(64) NOT NULL,
	ord int4 NOT NULL,
	"text" text NOT NULL,
	embedding public.vector NOT NULL,
	CONSTRAINT embeddings_refined_pkey PRIMARY KEY (id)
);
```
