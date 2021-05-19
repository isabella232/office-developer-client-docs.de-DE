---
title: Initialisieren des Transportanbieters
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 977c18ce-ece5-4ad1-ac97-5a680846ab83
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 474a8085ca8b82d11efd68c9fd4d8719fe239207
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33416601"
---
# <a name="initializing-the-transport-provider"></a>Initialisieren des Transportanbieters

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Die Transport-Spooler-Schnittstelle definiert Aufrufe, die der MAPI-Spooler an einen Transportanbieter macht. Transportanbieter implementieren diese Routinen in einer Dynamic Link Library (DLL). Der erste direkte Einstiegspunkt in die DLL, die vom MAPI-Spooler verwendet wird, muss die Initialisierungsfunktion des Transportanbieters [XPProviderInit sein.](xpproviderinit.md)
  
MAPI verwendet die Routine **GetProcAddress,** um die Adresse der Initialisierungsroutine des Dienstanbieters zu erhalten und diese Routine dann auf aufruft. Der Name der Initialisierungsroutine ist **XPProviderInit** für Transportanbieter. Bei anderen Typen von MAPI-Dienstanbietern ist dies unterschiedlich, sodass eine DLL eine beliebige Kombination von Dienstanbietertypen enthalten kann, jedoch nur einen Dienstanbieter eines bestimmten Typs. Ein Dienstanbieter eines bestimmten Typs kann jedoch mehrere Dienste seines Typs implementieren. Beispielsweise kann ein Transportanbieter die Nachrichtentransportfunktionalität in mehrere Nachrichtendienste implementieren. 
  
Die mapispi.h-Headerdatei verfügt über eine Typdefinition für den Funktionsprototyp der Initialisierungsfunktion des Transportanbieters und einen vordefinierten Prozedurnamen dafür. Indem Sie die Initialisierungsroutinen in Ihren C- und C++-Dateien mit denselben Namen benennen, die von **GetProcAddress** verwendet werden, und mithilfe einer einfachen Exportdeklaration in Ihrer DLL.DEF-Datei erhalten Sie automatisch die Typüberprüfung der Parameter in Ihrer Initialisierungsroutine. Beispiele finden Sie im Quellcode des Transportanbieters. Weitere Informationen finden Sie unter [Transport Provider Sample](transport-provider-sample.md).
  
Wenn der Initialisierungsaufruf eines Dienstanbieters erfolgreich ist, aber eine Versionsnummer der Dienstanbieterschnittstelle zurückgibt, die zu klein ist, damit MAPI verarbeiten kann, ruft MAPI sofort die **Release-Methode** des Dienstanbieterobjekts auf und geht so vor, als wäre der Initialisierungsaufruf mit MAPI_E_VERSION. Auf diese Weise definieren MAPI und der Dienstanbieter gemeinsam den Bereich der Dienstanbieterschnittstellenversionsnummern, die sie verarbeiten können, und wenn nichts mit dem Dienstanbieter zu tun hat, schlägt das Laden des Dienstanbieters mit einem MAPI_E_VERSION fehl. 
  
Der letzte Schritt für den MAPI-Spooler beim Abrufen des Zugriffs auf Dienstanbieterressourcen besteht in der Anmeldung beim Transportanbieter. Der MAPI-Spooler ruft die [IXPProvider::TransportLogon-Methode](ixpprovider-transportlogon.md) des [IXPProvider : IUnknown-Objekts](ixpprovideriunknown.md) auf, das von **XPProviderInit** zurückgegeben wird. Dies ist der Aufruf, bei dem Anmeldeinformationen aktiviert werden und Dialogfelder zulässig sind.
  
Wenn ein Prozess eine zweite Transportsitzung für denselben Transportanbieter und die gleiche MAPI-Sitzung öffnet, sollte die Transportanbieter-DLL kein zweites Anbieterobjekt erstellen. Das erste Anbieterobjekt sollte zum Anmelden bei der zweiten Transportsitzung verwendet werden. Ein Transportanbieter sollte so programmiert werden, dass mehrere Transportsitzungen in einem einzelnen Anbieterobjekt unterstützt werden. Ein zweites Anbieterobjekt sollte nur erstellt werden, wenn unterschiedliche MAPI-Sitzungen im gleichen Prozess verwendet werden.
  

