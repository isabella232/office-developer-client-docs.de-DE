---
title: Implementieren einer Einstiegspunktfunktion des Adressbuchanbieters
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 9375b351-1c84-4728-bcdf-e3e7a44820ed
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 00b3b30101ee1efb984cf45afb35b0b085d545ac
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409713"
---
# <a name="implementing-an-address-book-provider-entry-point-function"></a>Implementieren einer Einstiegspunktfunktion des Adressbuchanbieters

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Wenn eine Clientanwendung [MAPILogonEx](mapilogonex.md) aufruft, um eine Sitzung mit einem Profil zu beginnen, das Ihren Adressbuchanbieter enthält, lädt MAPI Ihren Anbieter und alle anderen, die Teil des Profils sind. MAPI erfährt den Namen der Einstiegspunktfunktion Ihres Anbieters, indem sie im Profil nachschaut. Beachten Sie, dass diese Funktion nicht mit einer #A0 identisch ist. Weitere Informationen finden Sie in der Dokumentation zu **DllMain** in der Win32-Dokumentation. 
  
Es gibt mehrere Einträge, von denen einige in der Konfigurationsdatei mapisvc.inf angezeigt werden müssen, die im Profilabschnitt jedes Adressbuchanbieters enthalten sind. In der folgenden Tabelle sind diese Profilabschnittseinträge aufgeführt, und ob die datei mapisvc.inf diese enthalten muss.
  
|**Profilabschnittseintrag**|**mapisvc.inf-Anforderung**|
|:-----|:-----|
|PR_DISPLAY_NAME= _Zeichenfolge_ <br/> |Optional.  <br/> |
|_PR_PROVIDER_DISPLAY=-Zeichenfolge_ <br/> |Erforderlich  <br/> |
|PR_PROVIDER_DLL_NAME= _DLL-Dateiname_ <br/> |Erforderlich  <br/> |
|PR_RESOURCE_TYPE= _long_ <br/> |Erforderlich  <br/> |
|PR_RESOURCE_FLAGS= _bitmask_ <br/> |Optional.  <br/> |
   
Ihr Adressbuchanbieter kann diese Informationen direkt in einem Profil platzieren, indem er die [IMAPIProp::SetProps-Methode des Profilabschnitts](imapiprop-setprops.md) aufruft oder indirekt MAPISVC.INF ändert. Profile werden mithilfe der relevanten Informationen in MAPISVC erstellt. INF für die ausgewählten Dienstanbieter oder Nachrichtendienste. Weitere Informationen zur Organisation und zum Inhalt von MAPISVC. INF, siehe [Dateiformat von MapiSvc.inf](file-format-of-mapisvc-inf.md).
  
Der Name der DLL-Einstiegspunktfunktion Ihres Adressbuchanbieters muss [ABProviderInit](abproviderinit.md) sein und dem **ABProviderInit-Prototyp** entsprechen. Führen Sie die folgenden Aufgaben in der DLL-Einstiegspunktfunktion Ihres Anbieters aus: 
  
- Überprüfen Sie die Version der Dienstanbieterschnittstelle (Service Provider Interface, SPI), um sicherzustellen, dass MAPI eine Version verwendet, die mit der Version kompatibel ist, die Ihr Adressbuchanbieter verwendet.
    
- Instanziieren eines Adressbuchanbieterobjekts.
    
Rufen Sie weder **MAPIInitialize** noch **MAPIUninitialize** in dieser Funktion auf. 
  
Die DLL-Einstiegspunktfunktion instanziiert ein Anbieterobjekt und gibt an MAPI einen Zeiger auf dieses Objekt zurück. 
  

