<template>
  <section class="d-flex justify-content-center align-items-center flex-column">
    <BoxContent
      compType="div"
      class="d-flex flex-column justify-content-center align-items-center"
    >
      <h3 class="text-center font-weight-bold mt-3">
        CATÁLOGO COM DESCRIÇÃO DOS PRODUTOS E SEUS VALORES
      </h3>
      <h5 class="text-center mt-3 mb-3">
        Vamos te contar alguns detalhes importantes, antes mesmo de você ver as
        fotos e as descrições de nossos produtos brincantes:
      </h5>
    </BoxContent>

    <b-list-group>
      <ListItem>
        No momento não temos produtos a pronta entrega. Seu pedido pode levar
        até 20 dias para ficar pronto + o prazo do frete, caso você não resida
        em Curitiba e Região Metropolitana de Curitiba.
      </ListItem>
      <ListItem>
        Todos os produtos brincantes são indicados para crianças maiores de 03
        anos por conterem partes pequenas.
      </ListItem>
      <ListItem>
        Tomamos todos os cuidados para que nossa costura e colagem fiquem
        firmes, mas mesmo assim...
      </ListItem>
      <ListItem>
        É sugerido que a criança explore os brinquedos/brinque com supervisão de
        um/a adulto/a (parte boa de entrar na brincadeira com a criançada!).
      </ListItem>
      <ListItem>
        Por serem artesanais, os produtos estão sujeitos a sutis alterações em
        seu formato e tamanho.
      </ListItem>
      <ListItem>
        Todos os produtos são confeccionados em feltro e/ou tecido; quando
        necessário utilizar base, a mesma é feita com papelão.
      </ListItem>
      <ListItem>
        Os valores informados podem sofrer alteração sem aviso prévio.
      </ListItem>
      <ListItem>
        Formas de Pagamento: PIX ou transferência bancária de 50% do valor do
        pedido de entrada e os outros 50% na entrega.
      </ListItem>
      <ListItem>
        <span>Aceitamos cartão de crédito para compras acima de
          <b>R$250,00</b></span>
      </ListItem>
      <ListItem>
        <b>Para efetivar seu pedido ou personalizá-lo entre em contato com a
          Mari pelo (41) 9 9693-5177.</b>
        <WhatsApp />
      </ListItem>
      <ListItem>
        Ou pelo Instagram! :)
        <Instagram />
      </ListItem>
    </b-list-group>
  </section>
</template>

<script>


export default {
  name: "TheHome",
};
</script>

<style scoped>
h5 {
  width: 70%;
}
</style>