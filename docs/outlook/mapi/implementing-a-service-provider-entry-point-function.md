---
title: Implementieren einer Service Provider Eintrag Point-Funktion
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 83ff54c4-86ce-4529-ae45-260dfb763b30
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 632aff9c0f6fc60ee9730b5e43667b5b610ae8df
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792543"
---
# <a name="implementing-a-service-provider-entry-point-function"></a>Implementieren einer Service Provider Eintrag Point-Funktion

  
  
**Betrifft**: Outlook 
  
Jeder Dienstanbieter DLL hat einen Eintrag Funktion verweist, die MAPI-aufrufen, um sie zu laden. Beachten Sie, dass dieser Eintrag Point-Funktion nicht [DllMain](http://msdn.microsoft.com/en-us/library/ms682583.aspx), die Win32-DLL-Einstiegspunktfunktion identisch ist.
  
Je nach Typ des vom Dienstanbieter entspricht anderer Prototyp Ihrem Anbieter Eintrag Point-Funktion. MAPI definiert anderen Eintrag Punkt Prototypen für Dienstanbieter.
  
|**Provider**|**Entry Point-Funktionsprototyp**|
|:-----|:-----|
|Nachricht-Anbieter  <br/> |[MSProviderInit](msproviderinit.md) <br/> |
|Transportanbieter  <br/> |[XPProviderInit](xpproviderinit.md) <br/> |
|Von adressbuchanbietern implementierte  <br/> |[ABProviderInit](abproviderinit.md) <br/> |
   
Die Funktionalität in diese Prototypen entspricht weitgehend für alle Typen von Service Provider. 
  
Adressbuch, Nachrichtenspeicher und Transportanbieter führen die folgenden zwei Hauptaufgaben in deren Entry Point-Funktionen:
  
1. Überprüfen Sie die Version der der Dienstanbieter-Schnittstelle (SPI) um sicherzustellen, dass MAPI eine Version verwendet, die mit der Version kompatibel ist, die Ihren Dienstanbieter verwendet. Verwenden Sie den _LpulMAPIVer_ -Parameter, der die MAPI SPI-Version enthält, und der _LpulProviderVer_ -Parameter, der Ihre Version SPI enthält, des Überprüfens. Diese Parameter sind nicht signierte 32-Bit-Ganzzahl bestehend aus drei Teilen: 
    
  - Bits 24 bis 31 stellen die Hauptversion dar.
    
  - Bits 16 bis 23 darstellen, die Nebenversion.
    
  - Die Bits 0 bis 15 darstellen den Update-Bezeichner. Obwohl die Nummer der Hauptversion selten geändert werden, die Nebenversionsnummer Änderungen bei jedem MAPI freigegeben wird und die SPI geändert wurde. Die Update-ID ist die Microsoft-interne Buildversion. Es wird verwendet, um Änderungen während der Entwicklung nachzuverfolgen. MAPI definiert die CURRENT_SPI_VERSION-Konstante, in der Headerdatei Mapispi.h an, dass der derzeitigen SPI-Version dokumentiert. Die Kontrollkästchen der Fehler MAPI_E_VERSION fehl, wenn Sie eine Version der SPI verwenden, die neuer als die Version, die MAPI verwendet wird.
    
2. Erstellt eine Instanz eines Objekts vom Anbieter. Da der Anbieter gestartet und mehrmals initialisiert werden kann, sollten Sie eine neue Instanz jedes Mal erstellen, die in diesem Fall. Anbieter werden mehrere Male gestartet, wenn sie in mehreren Profilen angezeigt werden, die von einem oder mehreren Clients gleichzeitig verwendet werden, oder wenn sie mehrere Male in einem einzigen Profil angezeigt werden. Nur wächst der Eintrag Point-Funktionsprototyp je nach den Typ des vom Dienstanbieter abweicht, den Typ der Provider-Objekt. 
    
    Wenn Sie eine Adressbuchanbieter schreiben, implementieren [IABProvider: IUnknown](iabprovideriunknown.md). Wenn Sie eine Nachricht Speicheranbieter schreiben, implementieren [IMSProvider: IUnknown](imsprovideriunknown.md). Weitere Informationen finden Sie unter [Message-Anbieter laden](loading-message-store-providers.md).
    
    Wenn Sie eine Adressbuchhierarchie schreiben, implementieren [IXPProvider: IUnknown](ixpprovideriunknown.md). Weitere Informationen finden Sie unter [der Adressbuchhierarchie initialisieren](initializing-the-transport-provider.md).
    
## <a name="see-also"></a>Siehe auch



[Starten von einem Dienstanbieter](starting-a-service-provider.md)

