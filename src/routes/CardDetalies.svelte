<div class="modal" style="display: {modalIsOpen ? 'block' : 'none'};">
    <div class="modal-content">
        <!-- svelte-ignore a11y-click-events-have-key-events -->
        <span class="close" on:click={closeModal}>&times;</span>
        <div class="title">
            <input type="text" name="title" id="title" bind:value={task.title}>
        </div>

        <div class="description">
            <label for="description">Description:</label>
            <br>
            <textarea name="description" id="description" cols="40" rows="5" bind:value={task.description}></textarea>
        </div>

        <div class="type">
            <label for="type">Type:</label>
                <select name="type" id="type" bind:value={task.type}>
                    <option value="family">Family</option>
                    <option value="work">Work</option>
                    <option value="community">Community</option>
                    <option value="money">Money</option>
                    <option value="myself">Myself</option>
                </select>
        </div>

        <div class="date">
            <label for="date">Date:</label>
            <input type="date" name="date" id="date" bind:value={task.date}>
        </div>

        <div class="done">
            <label for="done">Done:</label>
            <label class="switch">
                <input type="checkbox" name="done" id="done">
                <span class="slider round"></span>
              </label>
        </div>

        <div class="btns">
            <button>
                Delete
            </button>

            <button>
                Save
            </button>
        </div>
    </div>
</div>
  
  <script>
    export let modalIsOpen = false;

    export let task;
  
    function closeModal() {
      modalIsOpen = false;
    }
  </script>
  
  <style>
    .modal {
      position: fixed;
      top: 0;
      left: 0;
      width: 100%;
      height: 100%;
      background-color: rgba(0, 0, 0, 0.5);
      z-index: 9999;
    }
  
    .modal-content {
      background-color: white;
      padding: 1rem;
      border-radius: 0.5rem;
      position: absolute;
      top: 50%;
      left: 50%;
      transform: translate(-50%, -50%);
      max-width: 90%;
      max-height: 90%;
      overflow-y: auto;
    }
  
    .close {
      color: #aaa;
      float: right;
      font-size: 28px;
      font-weight: bold;
      margin-right: 0.5rem;
      margin-top: 0.2rem;
      cursor: pointer;
    }
    textarea {
        resize: none;
        background-color: aliceblue;
    }
    select {
        width: 100%;
    }
    #title {
        font-size: 20px;
        background-color: aliceblue;
    }

    #title, #description, #type, #date {
        border: none;
        background-color: #0cd4e63f;
        border-radius: 5px;
    }

    /* switcer */

    .switch {
    position: relative;
    display: inline-block;
    width: 30px;
    height: 17px;
    }

    /* Hide default HTML checkbox */
    .switch input {
    opacity: 0;
    width: 0;
    height: 0;
    }

    /* The slider */
    .slider {
    position: absolute;
    cursor: pointer;
    top: 0;
    left: 0;
    right: 0;
    bottom: 0;
    background-color: #ccc;
    -webkit-transition: .4s;
    transition: .4s;
    }

    .slider:before {
    position: absolute;
    content: "";
    height: 13px;
    width: 13px;
    left: 2px;
    bottom: 2px;
    background-color: white;
    -webkit-transition: .4s;
    transition: .4s;
    }

    input:checked + .slider {
    background-color: #2196F3;
    }

    input:focus + .slider {
    box-shadow: 0 0 1px #2196F3;
    }

    input:checked + .slider:before {
    -webkit-transform: translateX(13px);
    -ms-transform: translateX(13px);
    transform: translateX(13px);
    }

    .slider.round {
    border-radius: 34px;
    }

    .slider.round:before {
    border-radius: 50%;
    }
  </style>