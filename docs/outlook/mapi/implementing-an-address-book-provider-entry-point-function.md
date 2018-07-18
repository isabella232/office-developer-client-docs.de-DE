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
ms.openlocfilehash: b60a80bc0ede0c2800f6cfd98a98f498b93a1d8c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792547"
---
# <a name="implementing-an-address-book-provider-entry-point-function"></a>Implementieren einer Adressbuchanbieter-Einstiegspunktfunktion

  
  
**Betrifft**: Outlook 
  
Wenn ein Client Application aufruft [MAPILogonEx](mapilogonex.md) Beginn eine Sitzung mit einem Profil, das Ihre Adressbuchanbieter enthält, lädt MAPI Ihres Anbieters und alle anderen Personen, die Teil des Profils sind. MAPI lernen im Profil anhand des Namens des Anbieters Entry Point-Funktion. Beachten Sie, dass diese Funktion nicht mit einer DLL-Einstiegspunktfunktion ist. finden Sie in der Dokumentation für **DllMain** in der Win32-Dokumentation. 
  
Es sind mehrere Einträge, von die einige in der Konfigurationsdatei mapisvc.inf vorhanden sein muss, die im Profilabschnitt von jedem Adressbuchanbieter enthalten sind. Die folgende Tabelle enthält diese Profil Abschnitt Einträge und unabhängig davon, ob Sie die Datei "mapisvc.inf" umfassen werden muss.
  
|**Profil Abschnitt Eintrag**|**MAPISVC.inf-Anforderung**|
|:-----|:-----|
|PR_DISPLAY_NAME = _Zeichenfolge_ <br/> |Optional  <br/> |
|PR_PROVIDER_DISPLAY = _Zeichenfolge_ <br/> |Erforderlich  <br/> |
|PR_PROVIDER_DLL_NAME = _DLL-Dateiname_ <br/> |Erforderlich  <br/> |
|PR_RESOURCE_TYPE = _long_ <br/> |Erforderlich  <br/> |
|PR_RESOURCE_FLAGS = _Bitmaske_ <br/> |Optional  <br/> |
   
Ihre Adressbuchanbieter kann diese Informationen in einem Profil direkt durch Aufrufen der Benutzerprofildienst-Abschnitt [IMAPIProp::SetProps](imapiprop-setprops.md) -Methode oder indirekt durch Ändern der MAPISVC.INF platzieren. Profile basieren, verwenden die entsprechende Informationen in MAPISVC. INF-Datei für den ausgewählten Dienstanbieter oder Message-Dienste. Weitere Informationen über die Organisation und den Inhalt der Datei MAPISVC. INF-Datei, finden Sie unter [File Format der MapiSvc.inf](file-format-of-mapisvc-inf.md).
  
Der Name des Ihrer Adressbuchanbieter DLL-Einstiegspunktfunktion muss [ABProviderInit](abproviderinit.md) und muss mit dem **ABProviderInit** Prototyp entsprechen. Führen Sie die folgenden Aufgaben in Ihren Anbieter DLL-Einstiegspunktfunktion: 
  
- Überprüfen Sie die Version der der Dienstanbieter-Schnittstelle (SPI), um sicherzustellen, dass MAPI eine Version verwendet, die mit der Version kompatibel ist, die Ihre Adressbuchanbieter verwendet wird.
    
- Instanziieren Sie ein Address Book Anbieter-Objekt.
    
Rufen Sie **"MAPIInitialize"** oder **MAPIUninitialize** nicht in dieser Funktion. 
  
Die DLL-Einstiegspunktfunktion instanziiert ein Anbieterobjekt und gibt einen Zeiger auf dieses Objekt MAPI zurück. 
  

