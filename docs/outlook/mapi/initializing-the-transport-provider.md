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
ms.openlocfilehash: 3b369e20101bbaba5e246b2ef9f6ab3ed1771ef6
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22563555"
---
# <a name="initializing-the-transport-provider"></a>Initialisieren des Transportanbieters

  
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
Die Transport-Warteschlange-Schnittstelle definiert aufgerufen, der die MAPI-Warteschlange eines Transportdienstes gemacht werden. Transportanbieter implementieren diese Routinen in einer Dynamic-Link Library (DLL). Der erste direkte Einstiegspunkt in der DLL, die durch die MAPI-Warteschlange verwendet muss die Transport Anbieter Initialisierungsfunktion [XPProviderInit](xpproviderinit.md).
  
MAPI wird die Routine **GetProcAddress** verwendet, um die Adresse des Initialisierungsroutine des Dienstanbieters abzurufen und Sie erhalten diese Routine. Der Name des die Initialisierungsroutine ist **XPProviderInit** für Transportanbieter. Es ist für andere Typen von MAPI-Dienstanbieter, sodass eine DLL-Datei eine beliebige Kombination von Anbieter Diensttypen, jedoch nur ein Dienstanbieter eines bestimmten Typs enthalten kann. Einen Dienstanbieter eines bestimmten Typs kann jedoch mehrere Dienste dieses Typs implementieren. Beispielsweise kann eine Adressbuchhierarchie Nachricht Transport Funktionalität für mehrere Nachrichtendienste für die implementieren. 
  
Die Headerdatei mapispi.h verfügt über eine Typdefinition für die Funktionsprototyp der Initialisierungsfunktion Transport Anbieter und eine vordefinierte Prozedurname dafür. Durch die Initialisierung benennen Routinen in Ihrer C und C++-Dateien mit den gleichen Namen von **GetProcAddress** verwendet und mithilfe von ein einfaches exportieren Deklaration in der DLL. DEF-Datei, erhalten Sie automatisch der Parameter auf Ihre Initialisierungsroutine Überprüfung. Finden Sie unter dem Transport Anbieter Beispielquellcode für Beispiele. Weitere Informationen finden Sie unter [Transport Provider Sample](transport-provider-sample.md).
  
Wenn einem Dienstanbieter Initialisierungsaufruf erfolgreich ist, jedoch gibt einem Dienstanbieter Versionsnummer der Benutzeroberfläche für die Behandlung von MAPI zu klein, MAPI sofort die **Release** -Methode des Service Provider-Objekts aufgerufen und wird fortgesetzt, als ob die Initialisierung aufrufen Installationsfehler mit MAPI_E_VERSION. Auf diese Weise MAPI und dem Dienstanbieter gemeinsam definieren den Bereich von Service Provider-Schnittstelle Versionsnummern, die sie bearbeiten können, und wenn nichts entspricht-Dienstanbieter laden funktioniert nicht mit einem MAPI_E_VERSION-Wert zurück. 
  
Der letzte Schritt für die MAPI-Warteschlange in die erste Zugriff auf Service Provider Ressourcen ist zur Anmeldung bei der Adressbuchhierarchie. Die MAPI-Warteschlange Ruft die [IXPProvider::TransportLogon](ixpprovider-transportlogon.md) -Methode von der [IXPProvider: IUnknown](ixpprovideriunknown.md) Objekt aus der **XPProviderInit**zurückgegeben. Dies ist der Anruf, in denen Sie Anmeldeinformationen verwendet, werden geprüft und Dialogfelder zugelassen werden können.
  
Wenn ein Vorgang eine zweite Transport-Sitzung auf der gleichen Adressbuchhierarchie und MAPI-Sitzung geöffnet wird, sollte der Adressbuchhierarchie DLL kein zweites Anbieterobjekt erstellen. Das erste Anbieterobjekt sollte verwendet werden, an die zweite Transport-Sitzung anmelden. Ein Transportdienstes sollte so programmiert werden zur Unterstützung mehrerer Transport Sitzungen in einem einzigen Anbieter-Objekt. Ein zweites Anbieterobjekt sollte nur erstellt werden, wenn andere MAPI-Sitzungen in demselben Prozess verwendet werden.
  

