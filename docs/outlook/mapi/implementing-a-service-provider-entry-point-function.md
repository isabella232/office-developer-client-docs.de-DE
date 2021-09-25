---
title: Implementieren einer Dienstanbieter-Einstiegspunktfunktion
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 83ff54c4-86ce-4529-ae45-260dfb763b30
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 4a315c0d3ec4ebb32cf337d7c10009c2736c67d8
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59567319"
---
# <a name="implementing-a-service-provider-entry-point-function"></a>Implementieren einer Dienstanbieter-Einstiegspunktfunktion

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Jede Dienstanbieter-DLL verfügt über eine Einstiegspunktfunktion, die MAPI aufruft, um sie zu laden. Beachten Sie, dass diese Einstiegspunktfunktion nicht mit [dllMain](https://msdn.microsoft.com/library/ms682583.aspx), der Win32 DLL-Einstiegspunktfunktion, identisch ist.
  
Je nach Anbietertyp entspricht die Einstiegspunktfunktion des Anbieters einem anderen Prototyp. MAPI definiert verschiedene Einstiegspunktfunktionsprototypen für Dienstanbieter.
  
|**Provider**|**Prototyp der Einstiegspunktfunktion**|
|:-----|:-----|
|Nachrichtenspeicheranbieter  <br/> |[MSProviderInit](msproviderinit.md) <br/> |
|Transportanbieter  <br/> |[XPProviderInit](xpproviderinit.md) <br/> |
|Adressbuchanbieter  <br/> |[ABProviderInit](abproviderinit.md) <br/> |
   
Ein Großteil der Funktionalität in diesen Prototypen ist für alle Dienstanbietertypen identisch. 
  
Adressbuch-, Nachrichtenspeicher- und Transportanbieter führen die folgenden beiden Hauptaufgaben in ihren Einstiegspunktfunktionen aus:
  
1. Überprüfen Sie die Version der Dienstanbieterschnittstelle (SPI), um sicherzustellen, dass die MAPI eine Version verwendet, die mit der von Ihrem Dienstanbieter verwendeten Version kompatibel ist. Verwenden Sie den  _Parameter "lpulMAPIVer",_ der die MAPI-SPI-Version enthält, und den  _Parameter "lpulProviderVer",_ der Ihre SPI-Version enthält, um die Überprüfung durchzuführen. Diese Parameter sind 32-Bit-Ganzzahlen ohne Vorzeichen, die aus drei Teilen bestehen: 
    
  - Die Bits 24 bis 31 stellen die Hauptversion dar.
    
  - Die Bits 16 bis 23 stellen die Nebenversion dar.
    
  - Die Bits 0 bis 15 stellen den Updatebezeichner dar. Obwohl sich die Hauptversionsnummer nur selten ändert, ändert sich die Nebenversionsnummer bei jeder MAPI-Veröffentlichung und der SPI-Änderung. Der Updatebezeichner ist die interne Buildversion von Microsoft. Es wird verwendet, um Änderungen während des Entwicklungsprozesses nachzuverfolgen. MAPI definiert die CURRENT_SPI_VERSION Konstante, die in der Headerdatei Mapispi.h dokumentiert ist, um die aktuelle SPI-Version anzugeben. Führen Sie die Prüfung mit dem Fehler MAPI_E_VERSION, wenn Sie eine neuere SPI-Version als die von der MAPI verwendeten Version verwenden.
    
2. Erstellen sie eine Instanz eines Anbieterobjekts. Da Ihr Anbieter mehrmals gestartet und initialisiert werden kann, sollten Sie jedes Mal eine neue Instanz erstellen. Anbieter werden mehrmals gestartet, wenn sie in mehreren Profilen angezeigt werden, die gleichzeitig von einem oder mehreren Clients verwendet werden, oder wenn sie mehrmals in einem einzelnen Profil angezeigt werden. Ebenso wie sich der Prototyp der Einstiegspunktfunktion je nach Anbietertyp unterscheidet, gilt dies auch für den Typ des Anbieterobjekts. 
    
    Wenn Sie einen Adressbuchanbieter schreiben, implementieren [Sie IABProvider : IUnknown](iabprovideriunknown.md). Wenn Sie einen Nachrichtenspeicheranbieter schreiben, implementieren [Sie IMSProvider : IUnknown](imsprovideriunknown.md). Weitere Informationen finden Sie unter [Laden von Nachrichten Store Anbietern.](loading-message-store-providers.md)
    
    Wenn Sie einen Transportanbieter schreiben, implementieren [Sie IXPProvider : IUnknown](ixpprovideriunknown.md). Weitere Informationen finden Sie unter [Initialisieren des Transportanbieters.](initializing-the-transport-provider.md)
    
## <a name="see-also"></a>Siehe auch



[Starten eines Dienstanbieters](starting-a-service-provider.md)

