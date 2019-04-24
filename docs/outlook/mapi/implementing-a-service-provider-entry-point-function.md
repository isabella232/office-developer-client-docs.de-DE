---
title: Implementieren einer Dienstanbieter-Einstiegspunktfunktion
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 83ff54c4-86ce-4529-ae45-260dfb763b30
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 14dd11f873493e32b83dbd1960cac8ff8ef8e436
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32332991"
---
# <a name="implementing-a-service-provider-entry-point-function"></a>Implementieren einer Dienstanbieter-Einstiegspunktfunktion

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Jede Dienstanbieter-DLL verfügt über eine Einstiegspunktfunktion, die von MAPI aufgerufen wird, um Sie zu laden. Beachten Sie, dass diese Einstiegspunktfunktion nicht mit [DllMain](https://msdn.microsoft.com/library/ms682583.aspx), der Win32-DLL-Einstiegspunktfunktion, identisch ist.
  
Je nach Typ des Anbieters entspricht die Einstiegspunktfunktion des Anbieters einem anderen Prototyp. MAPI definiert unterschiedliche Prototypen für Einstiegspunktfunktionen für Dienstanbieter.
  
|**Provider**|**Prototyp der Einstiegspunktfunktion**|
|:-----|:-----|
|Nachrichtenspeicher Anbieter  <br/> |[MSProviderInit](msproviderinit.md) <br/> |
|Transport Anbieter  <br/> |[XPProviderInit](xpproviderinit.md) <br/> |
|Adressbuchanbieter  <br/> |[ABProviderInit](abproviderinit.md) <br/> |
   
Ein großer Teil der Funktionalität in diesen Prototypen ist für alle Dienstanbieter Typen identisch. 
  
Adressbuch, Nachrichtenspeicher und Transportanbieter führen die folgenden beiden Hauptaufgaben in ihren Einstiegspunktfunktionen aus:
  
1. Überprüfen Sie die Version der Service Provider Interface (SPI), um sicherzustellen, dass MAPI eine Version verwendet, die mit der Version kompatibel ist, die Ihr Dienstanbieter verwendet. Verwenden Sie den _lpulMAPIVer_ -Parameter, der die MAPI-SPI-Version enthält, und den _lpulProviderVer_ -Parameter, der Ihre SPI-Version enthält, um die Prüfung durchzuführen. Diese Parameter sind 32-Bit-Ganzzahlen ohne Vorzeichen aus drei Teilen: 
    
  - Die Bits 24 bis 31 stellen die Hauptversion dar.
    
  - Die Bits 16 bis 23 stellen die Nebenversion dar.
    
  - Die Bits 0 bis 15 stellen den Update Bezeichner dar. Obwohl sich die Hauptversionsnummer selten ändert, ändert sich die Versionsnummer der Nebenversion immer dann, wenn MAPI veröffentlicht und der SPI geändert wurde. Die Update-ID ist die interne Microsoft-Buildversion; Es wird verwendet, um Änderungen während des Entwicklungsprozesses nachzuverfolgen. MAPI definiert die CURRENT_SPI_VERSION-Konstante, die in der Headerdatei Mapispi. h dokumentiert ist, um die aktuelle SPI-Version anzugeben. Führen Sie die Überprüfung mit dem Fehler MAPI_E_VERSION aus, wenn Sie eine Version des SPI verwenden, die neuer als die von MAPI verwendete Version ist.
    
2. Erstellen Sie eine Instanz eines Provider-Objekts. Da Ihr Anbieter mehrmals gestartet und initialisiert werden kann, sollten Sie jedesmal eine neue Instanz erstellen. Anbieter werden mehrmals gestartet, wenn Sie in mehreren Profilen angezeigt werden, die gleichzeitig von einem oder mehreren Clients verwendet werden, oder wenn Sie mehrmals in einem einzigen Profil angezeigt werden. Ebenso wie der Prototyp der Einstiegspunktfunktion in Abhängigkeit vom Typ des Anbieters unterschiedlich ist, wird auch der Typ des Anbieterobjekts verwendet. 
    
    Wenn Sie einen Adressbuchanbieter schreiben, implementieren Sie [IABProvider: IUnknown](iabprovideriunknown.md). Wenn Sie einen Nachrichtenspeicher Anbieter schreiben, implementieren Sie [IMSProvider: IUnknown](imsprovideriunknown.md). Weitere Informationen finden Sie unter [Loading Message Store Providers](loading-message-store-providers.md).
    
    Wenn Sie einen Transportanbieter schreiben, implementieren Sie [IXPProvider: IUnknown](ixpprovideriunknown.md). Weitere Informationen finden Sie unter [Initialisieren des Transport Anbieters](initializing-the-transport-provider.md).
    
## <a name="see-also"></a>Siehe auch



[Starten eines Dienstanbieters](starting-a-service-provider.md)

