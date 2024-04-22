<template>
    <form @submit.prevent="cadastraTarefa">
        <div class="row">
        <div class="col">
            <input :value="estado.tarefaTemp" @change="eventos => estado.tarefaTemp = eventos.target.value" required type="text" class="form-control" placeholder="Digite aqui a descição da tarefa">
        </div>
        <div class="col-md-2">
            <button type="submit"class="btn btn-primary">Cadastrar</button>
        </div>
        <div class="col-md-2">
            <select @change="evento => estado.filtro = evento.target.value" class="form-control">
                <option value="todas">Todas tarefas</option>
                <option value="pendentes">pendentes</option>
                <option value="finalizadas">finalizadas</option>
            </select>
        </div>
        </div>
    </form>
</template>