---
title: Initialisieren des Transport Anbieters
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 977c18ce-ece5-4ad1-ac97-5a680846ab83
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 474a8085ca8b82d11efd68c9fd4d8719fe239207
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32309681"
---
# <a name="initializing-the-transport-provider"></a>Initialisieren des Transport Anbieters

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Die Transport-Spooler-Schnittstelle definiert Aufrufe, die der MAPI-Spooler an einen Transportanbieter stellt. Transport Anbieter implementieren diese Routinen in einer Dynamic Link Library (DLL). Der erste direkte Einstiegspunkt in die DLL, der vom MAPI-Spooler verwendet wird, muss die Initialisierungsfunktion des Transportanbieters [XPProviderInit](xpproviderinit.md)sein.
  
MAPI verwendet die Routine- **GetProcAddress** , um die Adresse der Initialisierungsroutine des Dienstanbieters abzurufen und diese Routine aufzurufen. Der Name der Initialisierungsroutine ist **XPProviderInit** für Transportanbieter. Es unterscheidet sich für andere Arten von MAPI-Dienstanbietern, sodass eine DLL eine beliebige Kombination von Dienstanbieter Typen enthalten kann, aber nur ein Dienstanbieter eines bestimmten Typs. Ein Dienstanbieter eines bestimmten Typs kann jedoch mehrere Dienste seines Typs implementieren. Ein Transportanbieter kann beispielsweise Nachrichtentransport Funktionen in mehrere Nachrichtendienste implementieren. 
  
Die Headerdatei mapispi. h enthält eine Typdefinition für den Funktionsprototyp der Initialisierungsfunktion des Transportanbieters und einen vordefinierten Prozedurnamen dafür. Durch Benennen der Initialisierungsroutinen in Ihren C-und C++-Dateien mit den gleichen Namen, die von **GetProcAddress** verwendet werden, und mithilfe einer einfachen Export Deklaration in der dll. DEF-Datei, erhalten Sie automatisch eine Typüberprüfung der Parameter in der Initialisierungsroutine. Beispiele finden Sie im Beispiel zum Transportanbieter-Quellcode. Weitere Informationen finden Sie unter [Transport Provider Sample](transport-provider-sample.md).
  
Wenn der Initialisierungsaufruf eines Dienstanbieters erfolgreich ist, aber die Versionsnummer einer Dienstanbieter-Schnittstelle zurückgibt, die für MAPI zu klein ist, ruft MAPI sofort die **Release** -Methode des dienstanbieterobjekts auf und fährt fort, als ob der Initialisierungsaufruf fehlgeschlagen mit MAPI_E_VERSION. Auf diese Weise definieren MAPI und der Dienstanbieter gemeinsam den Umfang der Versionsnummern der Dienstanbieter-Schnittstelle, die Sie verarbeiten können, und wenn nichts übereinstimmt, schlägt der Dienstanbieter Ladevorgang mit einem MAPI_E_VERSION-Rückgabewert fehl. 
  
Der letzte Schritt für den MAPI-Spooler beim Zugriff auf Dienstanbieter Ressourcen besteht darin, sich beim Transportanbieter anzumelden. Der MAPI-Spooler Ruft die [IXPProvider:: TransportLogon](ixpprovider-transportlogon.md) -Methode des [IXPProvider: IUnknown](ixpprovideriunknown.md) -Objekts auf, das von **XPProviderInit**zurückgegeben wird. Dies ist der Anruf, bei dem die Anmeldeinformationen, falls verwendet, aktiviert sind und Dialogfelder zugelassen werden können.
  
Wenn ein Prozess eine zweite Transportsitzung für denselben Transportanbieter und dieselbe MAPI-Sitzung öffnet, sollte die Transportanbieter-DLL kein zweites Anbieterobjekt erstellen. Das erste Anbieterobjekt sollte für die Anmeldung bei der zweiten Transportsitzung verwendet werden. Ein Transportanbieter sollte so programmiert werden, dass er mehrere Transportsitzungen in einem einzelnen Anbieterobjekt unterstützt. Ein zweites Provider-Objekt sollte nur erstellt werden, wenn im gleichen Prozess unterschiedliche MAPI-Sitzungen verwendet werden.
  

