---
title: Initialisieren des Transportanbieters
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 977c18ce-ece5-4ad1-ac97-5a680846ab83
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 36da5f2b2b5135c89480595da506eacc68d232cc
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59613891"
---
# <a name="initializing-the-transport-provider"></a>Initialisieren des Transportanbieters

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Die Transport-Spooler-Schnittstelle definiert Aufrufe, die der MAPI-Spooler an einen Transportanbieter sendet. Transportanbieter implementieren diese Routinen in einer Dynamic Link Library (DLL). Der erste direkte Einstiegspunkt in die DLL, die vom MAPI-Spooler verwendet wird, muss die Initialisierungsfunktion des Transportanbieters [XPProviderInit](xpproviderinit.md)sein.
  
MAPI verwendet die Routine **GetProcAddress,** um die Adresse der Initialisierungsroutine des Dienstanbieters abzurufen, und ruft dann diese Routine auf. Der Name der Initialisierungsroutine lautet **XPProviderInit** für Transportanbieter. Sie unterscheidet sich für andere Typen von MAPI-Dienstanbietern, sodass eine DLL eine beliebige Kombination von Dienstanbietertypen enthalten kann, jedoch nur einen Dienstanbieter eines bestimmten Typs. Ein Dienstanbieter eines bestimmten Typs kann jedoch mehrere Dienste seines Typs implementieren. Beispielsweise kann ein Transportanbieter Nachrichtentransportfunktionen in mehrere Nachrichtendienste implementieren. 
  
Die Headerdatei mapispi.h verfügt über eine Typdefinition für den Funktionsprototyp der Initialisierungsfunktion des Transportanbieters und einen vordefinierten Prozedurnamen dafür. Indem Sie die Initialisierungsroutinen in Ihren C- und C++-Dateien mit denselben Namen benennen, die von **GetProcAddress** verwendet werden, und indem Sie eine einfache Exportdeklaration in der DLL.DEF-Datei verwenden, erhalten Sie automatisch eine Typüberprüfung der Parameter für Ihre Initialisierungsroutine. Beispiele finden Sie im Beispiel für den Quellcode des Transportanbieters. Weitere Informationen finden Sie unter [Transport Provider Sample](transport-provider-sample.md).
  
Wenn der Initialisierungsaufruf eines Dienstanbieters erfolgreich ist, aber eine Versionsnummer der Dienstanbieterschnittstelle zurückgibt, die mapi zu klein für die Verarbeitung ist, ruft MAPI sofort die **Release-Methode** des Dienstanbieterobjekts auf und geht so vor, als ob der Initialisierungsaufruf mit MAPI_E_VERSION fehlgeschlagen wäre. Auf diese Weise definieren MAPI und der Dienstanbieter gemeinsam den Bereich der Dienstanbieter-Schnittstellenversionsnummern, die sie verarbeiten können. Wenn nichts mit dem Laden eines Dienstanbieters übereinstimmt, schlägt das Laden mit einem MAPI_E_VERSION Rückgabewert fehl. 
  
Der letzte Schritt für den MAPI-Spooler beim Zugriff auf Dienstanbieterressourcen besteht darin, sich beim Transportanbieter anzumelden. Der MAPI-Spooler ruft die [IXPProvider::TransportLogon-Methode](ixpprovider-transportlogon.md) des [IXPProvider : IUnknown-Objekts auf,](ixpprovideriunknown.md) das von **XPProviderInit** zurückgegeben wird. Dies ist der Aufruf, bei dem Anmeldeinformationen aktiviert sind und Dialogfelder zulässig sind, wenn sie verwendet werden.
  
Wenn ein Prozess eine zweite Transportsitzung für denselben Transportanbieter und die gleiche MAPI-Sitzung öffnet, sollte die Transportanbieter-DLL kein zweites Anbieterobjekt erstellen. Das erste Anbieterobjekt sollte verwendet werden, um sich bei der zweiten Transportsitzung anzumelden. Ein Transportanbieter sollte so programmiert werden, dass er mehrere Transportsitzungen in einem einzigen Anbieterobjekt unterstützt. Ein zweites Anbieterobjekt sollte nur erstellt werden, wenn verschiedene MAPI-Sitzungen im selben Prozess verwendet werden.
  

