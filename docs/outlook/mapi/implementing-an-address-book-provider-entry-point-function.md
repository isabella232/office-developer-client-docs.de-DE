---
title: Implementieren einer Adressbuchanbieter-Einstiegspunktfunktion
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 9375b351-1c84-4728-bcdf-e3e7a44820ed
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: d411ef555fe3cd3134bd28bfc66c85d32bda9859
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59610475"
---
# <a name="implementing-an-address-book-provider-entry-point-function"></a>Implementieren einer Adressbuchanbieter-Einstiegspunktfunktion

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Wenn eine Clientanwendung [MAPILogonEx](mapilogonex.md) aufruft, um eine Sitzung mit einem Profil zu beginnen, das Ihren Adressbuchanbieter enthält, lädt MAPI Ihren Anbieter und alle anderen, die Teil des Profils sind. MAPI erkennt den Namen der Einstiegspunktfunktion Ihres Anbieters, indem sie das Profil durchsieht. Denken Sie daran, dass diese Funktion nicht mit einer DLL-Einstiegspunktfunktion identisch ist. weitere Informationen finden Sie in der Dokumentation zu **DllMain** in der Win32-Dokumentation. 
  
Es gibt mehrere Einträge, von denen einige in der Konfigurationsdatei mapisvc.inf angezeigt werden müssen, die im Profilabschnitt jedes Adressbuchanbieters enthalten sind. In der folgenden Tabelle sind diese Profilabschnittseinträge aufgeführt, und es wird angegeben, ob sie in der Datei "mapisvc.inf" enthalten sein müssen.
  
|**Profilabschnittseintrag**|**mapisvc.inf-Anforderung**|
|:-----|:-----|
|PR_DISPLAY_NAME= _Zeichenfolge_ <br/> |Optional  <br/> |
|PR_PROVIDER_DISPLAY= _Zeichenfolge_ <br/> |Erforderlich  <br/> |
|PR_PROVIDER_DLL_NAME= _DLL-Dateiname_ <br/> |Erforderlich  <br/> |
|PR_RESOURCE_TYPE= _lang_ <br/> |Erforderlich  <br/> |
|PR_RESOURCE_FLAGS= _Bitmaske_ <br/> |Optional  <br/> |
   
Ihr Adressbuchanbieter kann diese Informationen direkt in einem Profil platzieren, indem er die [IMAPIProp::SetProps-Methode](imapiprop-setprops.md) des Profilabschnitts aufruft oder mapisvc.INF indirekt ändert. Profile werden anhand der relevanten Informationen in MAPISVC erstellt. INF für die ausgewählten Dienstanbieter oder Nachrichtendienste. Weitere Informationen zur Organisation und zum Inhalt von MAPISVC. INF, see [File Format of MapiSvc.inf](file-format-of-mapisvc-inf.md).
  
Der Name der DLL-Einstiegspunktfunktion Ihres Adressbuchanbieters muss [ABProviderInit](abproviderinit.md) sein und dem **ABProviderInit-Prototyp** entsprechen. Führen Sie die folgenden Aufgaben in der DLL-Einstiegspunktfunktion Ihres Anbieters aus: 
  
- Überprüfen Sie die Version der Dienstanbieterschnittstelle (SPI), um sicherzustellen, dass die MAPI eine Version verwendet, die mit der Version kompatibel ist, die Ihr Adressbuchanbieter verwendet.
    
- Instanziieren eines Adressbuchanbieterobjekts.
    
Rufen Sie in dieser Funktion weder **MAPIInitialize** noch **MAPIUninitialize** auf. 
  
Die DLL-Einstiegspunktfunktion instanziiert ein Anbieterobjekt und gibt an die MAPI einen Zeiger auf dieses Objekt zurück. 
  

