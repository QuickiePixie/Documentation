<template>
  <v-row class="flex flex-column justify-center align-center">
    <h2 class="h2 subheader">Quick Draw</h2>

    <v-row class="flex mt-5">
        <div class="canvas-container">
            <div>
                <v-row class="btn-toolbar" role="toolbar" aria-label="Toolbar with button groups">
                    <v-row class="btn-group py-2 px-3 my-2 flex align-center" role="group" aria-label="First group">
                      <button id="penBtn" type="button" class="btn btn-outline tool-btn">
                        <svg xmlns="http://www.w3.org/2000/svg" width="16" height="16" fill="currentColor" class="bi bi-pen icon" viewBox="0 0 16 16">
                            <path d="m13.498.795.149-.149a1.207 1.207 0 1 1 1.707 1.708l-.149.148a1.5 1.5 0 0 1-.059 2.059L4.854 14.854a.5.5 0 0 1-.233.131l-4 1a.5.5 0 0 1-.606-.606l1-4a.5.5 0 0 1 .131-.232l9.642-9.642a.5.5 0 0 0-.642.056L6.854 4.854a.5.5 0 1 1-.708-.708L9.44.854A1.5 1.5 0 0 1 11.5.796a1.5 1.5 0 0 1 1.998-.001m-.644.766a.5.5 0 0 0-.707 0L1.95 11.756l-.764 3.057 3.057-.764L14.44 3.854a.5.5 0 0 0 0-.708z"/>
                          </svg>
                      </button>
                      <button id="lineBtn" type="button" class="btn btn-outline tool-btn">
                        <svg xmlns="http://www.w3.org/2000/svg" width="16" height="16" fill="currentColor" class="bi bi-slash-lg" viewBox="0 0 16 16">
                            <path fill-rule="evenodd" d="M13.854 2.146a.5.5 0 0 1 0 .708l-11 11a.5.5 0 0 1-.708-.708l11-11a.5.5 0 0 1 .708 0"/>
                          </svg>
                      </button>
                      <button id="eraseBtn" type="button" class="btn btn-outline tool-btn">
                        <svg xmlns="http://www.w3.org/2000/svg" width="16" height="16" fill="currentColor" class="bi bi-eraser icon" viewBox="0 0 16 16">
                            <path d="M8.086 2.207a2 2 0 0 1 2.828 0l3.879 3.879a2 2 0 0 1 0 2.828l-5.5 5.5A2 2 0 0 1 7.879 15H5.12a2 2 0 0 1-1.414-.586l-2.5-2.5a2 2 0 0 1 0-2.828zm2.121.707a1 1 0 0 0-1.414 0L4.16 7.547l5.293 5.293 4.633-4.633a1 1 0 0 0 0-1.414zM8.746 13.547 3.453 8.254 1.914 9.793a1 1 0 0 0 0 1.414l2.5 2.5a1 1 0 0 0 .707.293H7.88a1 1 0 0 0 .707-.293z"/>
                          </svg>
                      </button>
                      <button id="bucketBtn" type="button" class="btn btn-outline tool-btn">
                        <svg xmlns="http://www.w3.org/2000/svg" width="16" height="16" fill="currentColor" class="bi bi-paint-bucket icon" viewBox="0 0 16 16">
                            <path d="M6.192 2.78c-.458-.677-.927-1.248-1.35-1.643a3 3 0 0 0-.71-.515c-.217-.104-.56-.205-.882-.02-.367.213-.427.63-.43.896-.003.304.064.664.173 1.044.196.687.556 1.528 1.035 2.402L.752 8.22c-.277.277-.269.656-.218.918.055.283.187.593.36.903.348.627.92 1.361 1.626 2.068.707.707 1.441 1.278 2.068 1.626.31.173.62.305.903.36.262.05.64.059.918-.218l5.615-5.615c.118.257.092.512.05.939-.03.292-.068.665-.073 1.176v.123h.003a1 1 0 0 0 1.993 0H14v-.057a1 1 0 0 0-.004-.117c-.055-1.25-.7-2.738-1.86-3.494a4 4 0 0 0-.211-.434c-.349-.626-.92-1.36-1.627-2.067S8.857 3.052 8.23 2.704c-.31-.172-.62-.304-.903-.36-.262-.05-.64-.058-.918.219zM4.16 1.867c.381.356.844.922 1.311 1.632l-.704.705c-.382-.727-.66-1.402-.813-1.938a3.3 3.3 0 0 1-.131-.673q.137.09.337.274m.394 3.965c.54.852 1.107 1.567 1.607 2.033a.5.5 0 1 0 .682-.732c-.453-.422-1.017-1.136-1.564-2.027l1.088-1.088q.081.181.183.365c.349.627.92 1.361 1.627 2.068.706.707 1.44 1.278 2.068 1.626q.183.103.365.183l-4.861 4.862-.068-.01c-.137-.027-.342-.104-.608-.252-.524-.292-1.186-.8-1.846-1.46s-1.168-1.32-1.46-1.846c-.147-.265-.225-.47-.251-.607l-.01-.068zm2.87-1.935a2.4 2.4 0 0 1-.241-.561c.135.033.324.11.562.241.524.292 1.186.8 1.846 1.46.45.45.83.901 1.118 1.31a3.5 3.5 0 0 0-1.066.091 11 11 0 0 1-.76-.694c-.66-.66-1.167-1.322-1.458-1.847z"/>
                          </svg>
                      </button>
                      <div class="" id="colorInput">
                        <input type="color" id="colorPicker" class="toolbar" value="#000000">
                      </div>
                      <div class="mx-4">
                        <select name="size" id="gridSize" class="toolbar">
                            <option value="128">S</option>
                            <option value="64">M</option>
                            <option value="32">L</option>
                            <option value="16">XL</option>
                          </select>
                          </div>
                </v-row>
            </v-row>
            <div class="pixel-grid bg-white">
                <canvas id="pixel-canvas" class="pixel-grid" width="512" height="512"> </canvas>
            </div>
            <v-row class="flex my-5">
                <div id="description"></div>
                <v-row class="w-100 flex">
                <v-btn class="w-50" id="createDescription">Create Description</v-btn>
                <h4 class="text-capitalize w-50 px-3" id="descriptionText" hidden></h4>
                </v-row>
                <v-row class="w-100 flex">
                <v-btn @click="downloadClick" class="w-50 mt-3" id="downloadImage">Save Image</v-btn>
                <h5 class="w-50 px-3" id="downloadText" style="overflow-wrap: break-word; font-size: 0.8rem;" hidden></h5>
                </v-row>
            </v-row>
        </div>
        </div>        
    </v-row>
  </v-row>
</template>


<style>
    * {
        box-sizing: border-box;
    }
    .header {
        font-size: 5rem;
    }

    .tool-btn {
        padding: 0.3rem;
        margin: 0.7rem;
        border-radius: 4px;
        border:3px solid transparent;
    }

    .tool-btn:hover {
        border:3px solid white;
    }

    .active-btn{
        border:3px solid white;
    }
    .canvas-container {
        width:100%;
        max-width: 600px;
        height:auto;
        margin:auto;
    }

</style>

<script setup>
import { onMounted } from 'vue'

const canvasSetup = () => {
    console.log("SETTING UP CANVAS")
const canvas = document.getElementById("pixel-canvas");
  const context = canvas.getContext("2d");

  //define grid size and pixel size
  let gridSize = 128;
  const canvasWidth = canvas.getBoundingClientRect().width;
  const screenScaling = canvas.width / canvasWidth;
  let pixelSize = canvasWidth / gridSize;

  const canvasSettings = {
    brush: "free",
    brushStart: [0, 0],
    currentColor: "black",
    isDrawing: false,
    isErasing: false,
  };

  canvas.addEventListener("mousedown", (event) => {
    if (canvasSettings.brush == "line") {
      startLine(event);
      return;
    } else if (canvasSettings.brush == "fill") {
      console.log("FILLING");
      const rect = canvas.getBoundingClientRect();
      const x = Math.floor((event.clientX - rect.left) / pixelSize);
      const y = Math.floor((event.clientY - rect.top) / pixelSize);
      const prevColor = colorPick(x, y);
      console.log(prevColor);
      fill(x, y, prevColor);
      return;
    } else if (canvasSettings.brush == "erase") {
      canvasSettings.isErasing = true;
    }
      canvasSettings.isDrawing = true;
      drawPixel(event);
  });

  canvas.addEventListener("mousemove", (event) => {
    if (canvasSettings.brush == "free" || canvasSettings.brush === "erase") drawPixel(event);
  });

  canvas.addEventListener("mouseup", (event) => {
    if (canvasSettings.brush == "line") {
      endLine(event);
    }
    canvasSettings.isErasing = false;
    canvasSettings.isDrawing = false;
    context.beginPath();
  });

  let gridDropDown = document.getElementById("gridSize");
  gridDropDown.addEventListener("change", (event) => {
    gridSize = parseInt(event.target.value);
    pixelSize = canvasWidth / gridSize;
    console.log(gridSize);
  });

  function drawPixel(event) {
    if (!canvasSettings.isDrawing) {
      return;
    }
    const rect = canvas.getBoundingClientRect();
    console.log(rect);
    const x = Math.floor((event.clientX - rect.left) / pixelSize);
    const y = Math.floor((event.clientY - rect.top) / pixelSize);

    console.log(`Drawing at (${x}, ${y})`);

    context.fillStyle = canvasSettings.currentColor;
    if (canvasSettings.isErasing) {
      context.clearRect(
        x * pixelSize * screenScaling,
        y * pixelSize * screenScaling,
        pixelSize * screenScaling,
        pixelSize * screenScaling
      );
      console.log("Erasing");
    } else {
      context.fillRect(
        x * pixelSize * screenScaling,
        y * pixelSize * screenScaling,
        pixelSize * screenScaling,
        pixelSize * screenScaling
      );
    }
  }

  function colorPick(x, y) {
    const pixelData = context.getImageData(
      x * pixelSize * screenScaling + 1,
      y * pixelSize * screenScaling + 1,
      1,
      1
    ).data;
    return pixelData;
  }

  function colorMatch(a, b) {
    return a[0] === b[0] && a[1] === b[1] && a[2] === b[2] && a[3] === b[3];
  }

  function fill(x, y, prevColor) {
    console.log(`Filling at (${x}, ${y})`);

    let stack = [[x, y]];
    console.log("stack", JSON.stringify(stack));
    const newColor = canvasSettings.currentColor;

    while(stack.length > 0){
        const [curX, curY] = stack.pop();
        if (curX < 0 || curX >= gridSize || curY < 0 || curY >= gridSize) continue;
        const currColor = colorPick(curX, curY);
        if (colorMatch(currColor, prevColor)) {
            context.fillStyle = newColor;
            context.fillRect(
                curX * pixelSize * screenScaling,
                curY * pixelSize * screenScaling,
                pixelSize * screenScaling,
                pixelSize * screenScaling
              );
            stack.push([curX+1, curY]);
            stack.push([curX-1, curY]);
            stack.push([curX, curY+1]);
            stack.push([curX, curY-1]);
        }
    }
  }

  function startLine(event) {
    const rect = canvas.getBoundingClientRect();
    const x = Math.floor((event.clientX - rect.left) / pixelSize);
    const y = Math.floor((event.clientY - rect.top) / pixelSize);
    canvasSettings.brushStart = [x, y];
  }

  function endLine(event) {
    const rect = canvas.getBoundingClientRect();
    const x = Math.floor((event.clientX - rect.left) / pixelSize);
    const y = Math.floor((event.clientY - rect.top) / pixelSize);
    const startX = canvasSettings.brushStart[0];
    const startY = canvasSettings.brushStart[1];

    let curX;
    let curY;

    let fullSlope = 0;
    if (x != startX && y != startY) fullSlope = (y - startY) / (x - startX);
    else if (x == startX) fullSlope = y - startY;
    else fullSlope = 0;
    const x0 = Math.min(startX, x);
    const x1 = Math.max(startX, x);
    curY = (x0 == startX ? startY : y) + 0.5;
    for (let i = x0; i <= x1; i += 1) {
      curX = i;
      curY += x0 == startX ? fullSlope : fullSlope;
      context.fillStyle = canvasSettings.currentColor;
      const drawX = curX * screenScaling;
      for (let j = 0; j <= Math.abs(fullSlope); j++) {
        const drawY = Math.floor(curY - j * Math.sign(fullSlope));
        if (drawY >= Math.min(startY, y) && drawY <= Math.max(y, startY))
          context.fillRect(
            drawX * pixelSize,
            drawY * screenScaling * pixelSize,
            pixelSize * screenScaling,
            pixelSize * screenScaling
          );
        else break;
      }
    }
  }

  /*
   ************************************************************
   */

  const createDescriptionButton = document.getElementById("createDescription");
  const descriptionText = document.getElementById("descriptionText");
    createDescriptionButton.addEventListener("click", async event => {
        canvas.toBlob(async (imageBlob) => {
            const formData = new FormData();
            formData.append("image", imageBlob);
            fetch(`https://imageanalyzer-be03.onrender.com/`, {
                method: 'POST',
                body: formData,
            })
                .then(response => response.json())
                .then(data => {
                    data = data.charAt(0).toUpperCase() + data.slice(1) + ".";
                    descriptionText.innerHTML = data;
                    descriptionText.hidden = false;
                })        
        }); 
    });

  const penButton = document.getElementById("penBtn");
  penButton.addEventListener("click", async (e) => {
    let toolBtns = Array.from(document.getElementsByClassName("tool-btn"));
    toolBtns.forEach((element) => {
      console.log(element.id);
      if (
        element.id != e.target.id &&
        element.classList.contains("active-btn")
      ) {
        element.classList.remove("active-btn");
      }
    });
    penButton.classList.add("active-btn");

    // call pen tool
    canvasSettings.brush = "free";
  });

  const lineButton = document.getElementById("lineBtn");
  lineButton.addEventListener("click", async (e) => {
    let toolBtns = Array.from(document.getElementsByClassName("tool-btn"));
    toolBtns.forEach((element) => {
      console.log(element.id);
      if (
        element.id != e.target.id &&
        element.classList.contains("active-btn")
      ) {
        element.classList.remove("active-btn");
      }
    });
    lineButton.classList.add("active-btn");

    // call pen tool
    canvasSettings.brush = "line";
  });

  const eraseButton = document.getElementById("eraseBtn");
  eraseButton.addEventListener("click", async (e) => {
    let toolBtns = Array.from(document.getElementsByClassName("tool-btn"));
    toolBtns.forEach((element) => {
      console.log(element.id);
      if (
        element.id != e.target.id &&
        element.classList.contains("active-btn")
      ) {
        element.classList.remove("active-btn");
      }
    });
    eraseButton.classList.add("active-btn");

    // call erase tool
    canvasSettings.brush = "erase";
  });

  const bucketButton = document.getElementById("bucketBtn");
  bucketButton.addEventListener("click", async (e) => {
    let toolBtns = Array.from(document.getElementsByClassName("tool-btn"));
    toolBtns.forEach((element) => {
      console.log(element.id);
      if (
        element.id != e.target.id &&
        element.classList.contains("active-btn")
      ) {
        element.classList.remove("active-btn");
      }
    });
    bucketButton.classList.add("active-btn");

    // call bucket tool
    canvasSettings.brush = "fill";
  });

  const colorPicker = document.getElementById("colorPicker");
  colorPicker.addEventListener("change", async (e) => {
    console.log(e.target.value);
    //call colour function
    canvasSettings.currentColor = e.target.value;
  });

    
    const downloadImageButton = document.getElementById("downloadImage");
    downloadImageButton.addEventListener("click", async () => {
        console.log("CKICKEDDOWNLOAD")
      const canvas = document.getElementById("pixel-canvas");
      const formData = new FormData();
      canvas.toBlob(async (imageBlob) => {
        formData.append("image", imageBlob)
        fetch(`${import.meta.env.VITE_APP_BACKEND_URL}/image`, {
          method: "POST",
          body: formData
        }).then(res => res.json())
        .then(data =>{
          const id = data.id;
          const elmt = document.getElementById("downloadText");
          elmt.hidden=false;
          elmt.innerText = `External Link: https://quickie-pixie-docs.vercel.app/image/${id}`;
        })
      });
    });
    downloadImageButton.disabled = false;
    createDescriptionButton.disabled = false;
}

onMounted(canvasSetup);

</script>