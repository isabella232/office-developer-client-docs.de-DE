---
title: Implementieren einer Adressbuchanbieter-Einstiegspunktfunktion
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 9375b351-1c84-4728-bcdf-e3e7a44820ed
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 00b3b30101ee1efb984cf45afb35b0b085d545ac
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32332802"
---
# <a name="implementing-an-address-book-provider-entry-point-function"></a>Implementieren einer Adressbuchanbieter-Einstiegspunktfunktion

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Wenn eine Clientanwendung [MAPILogonEx](mapilogonex.md) aufruft, um eine Sitzung mit einem Profil zu beginnen, das Ihren Adressbuchanbieter enthält, lädt MAPI Ihren Anbieter und alle anderen Teil des Profils. MAPI lernt den Namen der Einstiegspunktfunktion Ihres Anbieters, indem er im Profil nachsieht. Beachten Sie, dass diese Funktion nicht mit einer DLL-Einstiegspunktfunktion identisch ist. Weitere Informationen finden Sie in der Dokumentation zu **DllMain** in der Win32-Dokumentation. 
  
Es gibt mehrere Einträge, von denen einige in der MAPISVC. inf-Konfigurationsdatei enthalten sein müssen, die im profile-Abschnitt jedes Adressbuch Anbieters aufgeführt sind. In der folgenden Tabelle sind diese Profil Abschnitts Einträge aufgeführt, und ob die Datei MAPISVC. inf Diese enthält.
  
|**Profil Abschnitts Eintrag**|**MAPISVC. inf-Anforderung**|
|:-----|:-----|
|PR_DISPLAY_NAME = _Zeichenfolge_ <br/> |Optional  <br/> |
|PR_PROVIDER_DISPLAY = _Zeichenfolge_ <br/> |Erforderlich  <br/> |
|PR_PROVIDER_DLL_NAME = _dll filename_ <br/> |Erforderlich  <br/> |
|PR_RESOURCE_TYPE = _Long_ <br/> |Erforderlich  <br/> |
|PR_RESOURCE_FLAGS = _Bitmaske_ <br/> |Optional  <br/> |
   
Ihr Adressbuchanbieter kann diese Informationen direkt in einem Profil platzieren, indem er die [IMAPIProp::](imapiprop-setprops.md) SetProps-Methode des Profil Abschnitts oder indirekt durch Ändern von MAPISVC. inf aufruft. Profile werden mithilfe der relevanten Informationen in MAPISVC erstellt. INF für die ausgewählten Dienstanbieter oder Nachrichtendienste. Weitere Informationen zur Organisation und zu den Inhalten von MAPISVC. INF finden Sie unter [Datei Format von MapiSvc. inf](file-format-of-mapisvc-inf.md).
  
Der Name der DLL-Einstiegspunktfunktion Ihres Adressbuch Anbieters muss [ABProviderInit](abproviderinit.md) sein und dem **ABProviderInit** -Prototyp entsprechen. Führen Sie die folgenden Aufgaben in der DLL-Einstiegspunktfunktion Ihres Anbieters aus: 
  
- Überprüfen Sie die Version der Dienstanbieterschnittstelle (SPI), um sicherzustellen, dass MAPI eine Version verwendet, die mit der Version kompatibel ist, die ihr Adressbuchanbieter verwendet.
    
- Instanziieren eines Adressbuchanbieter Objekts.
    
Rufen Sie in dieser Funktion weder **MAPIInitialize** noch **MAPIUninitialize** auf. 
  
Die DLL-Einstiegspunktfunktion instanziiert ein Provider-Objekt und gibt einen Zeiger auf dieses Objekt an MAPI zurück. 
  

