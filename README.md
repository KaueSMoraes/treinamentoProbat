# treinamentoProbat
Treinamento Probat.
/*/{Protheus.doc} TestIntegracaoFinanceiro
    Teste de integração entre vendas e financeiro
    @type  Function
/*/
Function TestIntegracaoFinanceiro()
    Local oTest := ProbatTest():New()
    Local cPedido := ""
    Local aTitulos := {}
    
    oTest:SetTestSuite("Integração Financeiro")
    
    oTest:AddTest("Gerar Título ao Confirmar Pedido", {||
        // Cria pedido
        cPedido := CriarPedidoVenda()
        
        // Confirma pedido
        ConfirmarPedido(cPedido)
        
        // Verifica se títulos foram gerados
        aTitulos := BuscarTitulos(cPedido)
        
        Assert(Len(aTitulos) > 0, "Títulos devem ser gerados")
        Assert(aTitulos[1]:Status == "ABERTO", "Título deve estar aberto")
    })
    
    oTest:Run()
    
Return