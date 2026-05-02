# nanoGPT-practical
ask 2: Shakespeare Character-level Model
Generated samples (first 5 lines):

KING RICHARD III:
O, my good lord, I would thou wert not here!

QUEEN ELIZABETH:
And I, that I had never been thy queen!
Task 3: Model Architecture Exploration
Settings Tested (n_layer=7, varying heads):

Heads = 2: Loss = 1.1727
Heads = 3: Loss = 1.1691
Heads = 5: Loss = 1.1537
Heads = 7: Loss = 1.1355
Results: The lowest validation loss achieved was 1.1355. The best settings that produced this result were:

Layers: 7
Heads: 7
The plot of Loss vs. Number of Heads is saved in figures/loss_vs_heads.png.

Task 4: Training BabyGPT for Code Generation
Dataset:

Open-source C/C++ code from GitHub (raylib).
Computed tokens: 1,463,782 tokens (train) / 162,643 tokens (val).
Generated code samples (first 20 lines):

                   batch.vertexBuffer[i].vboId[1]);
                      onencodedData = (unsigned char)((float)font.glyphs[index].indth = (float)nangle;
                       glyphs[k].image->skizeofcets[i].image.data = rlGetPicelor(textData);

---------------

                   (unsigned int a0 = 0x0000000000000, 0x000000000, 0x000000,
          0x0000000, 0x80000000, 0x0000000, 0x000000000 };
         {(float *r + 1, (float)posX + 1, w3
             { (start0 + segments);
             }
             else if (image->format != NULL)                       
---------------

              glBufferSubBufferProcessedClearBitmp, RAGLTERACELOG(RL_LOG_WARNING, "GL: Callback and allowe= wave.channels, esting, downes[k]->translates[k].keyframePoses[i][j].texcoords[j]];
                    currentEventList->events[currentEventList->count].parent = currentPoint;
Favorite generated snippet:

             { (start0 + segments);
             }
             else if (image->format != NULL) 
Reason: Despite being trained on a very small dataset for a short time on a character level, the model successfully learned standard C/C++ formatting, pointer dereferencing (->), and structural keywords (else if).
