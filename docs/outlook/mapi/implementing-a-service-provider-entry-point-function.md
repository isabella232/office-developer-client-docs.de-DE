---
title: Implementieren einer Einstiegspunktfunktion des Dienstanbieters
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
# <a name="implementing-a-service-provider-entry-point-function"></a>Implementieren einer Einstiegspunktfunktion des Dienstanbieters

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Jede Dienstanbieter-DLL verfügt über eine Einstiegspunktfunktion, die MAPI aufruft, um sie zu laden. Beachten Sie, dass diese Einstiegspunktfunktion nicht mit [dllMain](https://msdn.microsoft.com/library/ms682583.aspx), der Win32-DLL-Einstiegspunktfunktion, identisch ist.
  
Je nach Typ Ihres Anbieters entspricht Ihre Anbieter-Einstiegspunktfunktion einem anderen Prototyp. MAPI definiert unterschiedliche Einstiegspunktfunktionsprototypen für Dienstanbieter.
  
|**Provider**|**Prototyp der Einstiegspunktfunktion**|
|:-----|:-----|
|Anbieter von Nachrichtenspeichern  <br/> |[MSProviderInit](msproviderinit.md) <br/> |
|Transportanbieter  <br/> |[XPProviderInit](xpproviderinit.md) <br/> |
|Adressbuchanbieter  <br/> |[ABProviderInit](abproviderinit.md) <br/> |
   
Ein Teil der Funktionalität in diesen Prototypen ist für alle Dienstanbietertypen identisch. 
  
Adressbuch-, Nachrichtenspeicher- und Transportanbieter führen die folgenden beiden Hauptaufgaben in ihren Einstiegspunktfunktionen aus:
  
1. Überprüfen Sie die Version der Dienstanbieterschnittstelle (SPI), um sicherzustellen, dass MAPI eine Version verwendet, die mit der version kompatibel ist, die Ihr Dienstanbieter verwendet. Verwenden Sie  _den lpulMAPIVer-Parameter,_ der die MAPI-SPI-Version enthält, und den  _lpulProviderVer-Parameter,_ der Ihre SPI-Version enthält, um die Überprüfung durchzuführen. Bei diesen Parametern handelt es sich um 32-Bit-Ganzzahlen ohne Vorzeichen, die aus drei Teilen bestehen: 
    
  - Bits 24 bis 31 stellen die Hauptversion dar.
    
  - Bits 16 bis 23 stellen die Nebenversion dar.
    
  - Bits 0 bis 15 stellen den Updatebezeichner dar. Obwohl sich die Hauptversionsnummer nur selten ändert, ändert sich die Nebenversionsnummer, sobald MAPI veröffentlicht wird und der SPI geändert wurde. Bei der Update-ID handelt es sich um die interne Buildversion von Microsoft. Es wird verwendet, um Änderungen während des Entwicklungsprozesses nachverfolgt. MAPI definiert die CURRENT_SPI_VERSION, die in der Mapispi.h-Headerdatei dokumentiert ist, um die aktuelle SPI-Version anzugeben. Führen Sie bei der Überprüfung einen Fehler MAPI_E_VERSION, wenn Sie eine Version des SPI verwenden, die neuer ist als die version, die MAPI verwendet.
    
2. Erstellen Sie eine Instanz eines Anbieterobjekts. Da Ihr Anbieter mehrmals gestartet und initialisiert werden kann, sollten Sie jedes Mal eine neue Instanz erstellen. Anbieter werden mehrmals gestartet, wenn sie in mehreren Profilen angezeigt werden, die gleichzeitig von einem oder mehreren Clients verwendet werden, oder wenn sie mehrmals in einem einzelnen Profil angezeigt werden. Ebenso wie sich der Prototyp der Einstiegspunktfunktion je nach Anbietertyp unterscheidet, gilt auch der Typ des Anbieterobjekts. 
    
    Wenn Sie einen Adressbuchanbieter schreiben, implementieren Sie [IABProvider : IUnknown](iabprovideriunknown.md). Wenn Sie einen Nachrichtenspeicheranbieter schreiben, implementieren [Sie IMSProvider : IUnknown](imsprovideriunknown.md). Weitere Informationen finden Sie unter [Loading Message Store Providers](loading-message-store-providers.md).
    
    Wenn Sie einen Transportanbieter schreiben, implementieren [Sie IXPProvider : IUnknown](ixpprovideriunknown.md). Weitere Informationen finden Sie unter [Initializing the Transport Provider](initializing-the-transport-provider.md).
    
## <a name="see-also"></a>Siehe auch



[Starten eines Dienstanbieters](starting-a-service-provider.md)

