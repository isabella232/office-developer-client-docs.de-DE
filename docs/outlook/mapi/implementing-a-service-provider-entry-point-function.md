---
title: Implementieren einer Dienstanbieter-Einstiegspunkte Funktion
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 83ff54c4-86ce-4529-ae45-260dfb763b30
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 14dd11f873493e32b83dbd1960cac8ff8ef8e436
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32332991"
---
# <a name="implementing-a-service-provider-entry-point-function"></a>Implementieren einer Dienstanbieter-Einstiegspunkte Funktion

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Jede Dienstanbieter-dll verfügt über eine Einstiegspunkte Funktion, die von MAPI-aufrufen zum Laden verwendet wird. Beachten Sie, dass diese Einstiegspunkte Funktion nicht mit [DllMain](https://msdn.microsoft.com/library/ms682583.aspx), der Win32-DLL-Einstiegspunkte Funktion identisch ist.
  
Je nach Typ Ihres Anbieters entspricht die Funktion des Anbieter Einstiegs Points einem anderen Prototyp. MAPI definiert unterschiedliche Einstiegspunkte-Funktionsprototypen für Dienstanbieter.
  
|**Provider**|**Einstiegspunkte-Funktionsprototyp**|
|:-----|:-----|
|Nachrichtenspeicher Anbieter  <br/> |[MSProviderInit](msproviderinit.md) <br/> |
|Transport Anbieter  <br/> |[XPProviderInit](xpproviderinit.md) <br/> |
|Adressbuchanbieter  <br/> |[ABProviderInit](abproviderinit.md) <br/> |
   
Ein Großteil der Funktionen in diesen Prototypen ist für alle Dienstanbieter Typen gleich. 
  
Adressbuch, Nachrichtenspeicher und Transportanbieter führen die folgenden zwei Hauptaufgaben in ihren Einstiegspunkten aus:
  
1. Überprüfen Sie die Version der Dienstanbieterschnittstelle (Service Provider Interface, SPI), um sicherzustellen, dass MAPI eine Version verwendet, die mit der Version kompatibel ist, die Ihr Dienstanbieter verwendet. Verwenden Sie den _lpulMAPIVer_ -Parameter, der die MAPI-SPI-Version enthält, und den _lpulProviderVer_ -Parameter, der Ihre SPI-Version enthält, um die Überprüfung durchzuführen. Bei diesen Parametern handelt es sich um 32-Bit-Ganzzahlen ohne Vorzeichen, die aus drei Teilen bestehen: 
    
  - Die Bits 24 bis 31 stellen die Hauptversion dar.
    
  - Die Bits 16 bis 23 stellen die Nebenversion dar.
    
  - Bits 0 bis 15 stellen die Update-ID dar. Die Hauptversionsnummer ändert sich zwar selten, aber die Nebenversionsnummer ändert sich immer dann, wenn MAPI freigegeben wird und sich der SPI geändert hat. Die Update-ID ist die interne Version von Microsoft Build; Sie wird zum Nachverfolgen von Änderungen während des Entwicklungsprozesses verwendet. MAPI definiert die CURRENT_SPI_VERSION-Konstante, die in der Headerdatei Mapispi. h dokumentiert ist, um die vorliegende SPI-Version anzugeben. Fehler bei der Überprüfung mit dem Fehler MAPI_E_VERSION, wenn Sie eine Version des SPI verwenden, die neuer ist als die von MAPI verwendete Version.
    
2. Erstellen Sie eine Instanz eines Provider-Objekts. Da Ihr Anbieter mehrmals gestartet und initialisiert werden kann, sollten Sie jedesmal eine neue Instanz erstellen. Anbieter werden mehrmals gestartet, wenn Sie in mehreren Profilen angezeigt werden, die gleichzeitig von einem oder mehreren Clients verwendet werden, oder wenn Sie mehrere Male in einem einzelnen Profil angezeigt werden. Ebenso wie der Prototyp der Einstiegsfunktion in Abhängigkeit vom Typ des Anbieters unterscheidet, wird auch der Typ des Anbieterobjekts verwendet. 
    
    Wenn Sie einen Adressbuchanbieter schreiben, implementieren Sie [IABProvider: IUnknown](iabprovideriunknown.md). Wenn Sie einen Nachrichtenspeicher Anbieter schreiben, implementieren Sie [IMSProvider: IUnknown](imsprovideriunknown.md). Weitere Informationen finden Sie unter [Laden von Nachrichtenspeicher Anbietern](loading-message-store-providers.md).
    
    Wenn Sie einen Transportanbieter schreiben, implementieren Sie [IXPProvider: IUnknown](ixpprovideriunknown.md). Weitere Informationen finden Sie unter [Initialisieren des Transport Anbieters](initializing-the-transport-provider.md).
    
## <a name="see-also"></a>Siehe auch



[Starten eines Dienstanbieters](starting-a-service-provider.md)

