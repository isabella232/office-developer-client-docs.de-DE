---
title: MAPI-Rückgabewert Dokumentation
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: c32ee53c-b063-4a00-a6bf-75ce5e07f56a
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 39d195f3cea6acbd5d5ab80cbba9d041ce9f7137
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22589147"
---
# <a name="mapi-return-value-documentation"></a>MAPI-Rückgabewert Dokumentation

  
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
Der Verweis Einträge in dieser Referenz des Dokuments nur diese Werte zurückgeben, die einige Behandlung von Clientanwendungen erfordern. Rückgabewerte, die allgemeine fehlerbedingungen anzugeben und Mobilgeräts auf eventuelle Fehler abgeleitet werden können, sind nicht in der Dokumentation enthalten. Beispielsweise können viele Schnittstellenmethoden MAPI_E_INVALID_PARAMETER zurück, wenn ein Anrufer gibt den falschen Wert für einen Eingabeparameter an. Dieser Wert wird in der Regel nicht in den erwarteten Rückgabewerte aufgeführt, weil es muss speziell für MAPI_E_INVALID_PARAMETER und müssen nicht anders aus einem anderen Fehler die Verarbeitung. Andererseits, einige Dienstanbieter unterstützen keine Benachrichtigung und MAPI_E_NO_SUPPORT an die Clients über **IMAPISession**vorgenommene **Advise** -Methode zurückgegeben werden. Da Clients müssen explizit für diesen Wert überprüfen und bereitstellen, sollten Code für die Behandlung der Bedingung, die es darstellt es tritt auf, MAPI_E_NO_SUPPORT ist in der Liste der Rückgabewerte für [IMAPISession::Advise](imapisession-advise.md)enthalten.
  
In der folgenden Tabelle werden die Fehlerwerte, die häufig von Methoden und Funktionen zurückgegeben werden und erfordern explizite Behandlung durch einen Client oder Dienstanbieter beschrieben. Diese Werte werden in vier Kategorien unterteilt: Werte, die ungültige Eingabedaten angeben, Werte, die Ressourcenprobleme hinweisen, Werte, die angeben, Zeichensatz Inkompatibilität und Werte, die Ausfall eines unbekannten Ursprungs angeben.
  
|**Rückgabewert**|**Beschreibung**|
|:-----|:-----|
|MAPI_E_INVALID_PARAMETER  <br/> |Eine oder mehrere der Parameter an die Methode übergebenen oder Funktionen sind nicht gültig.  <br/> |
|MAPI_E_UNKNOWN_FLAGS  <br/> |Eine oder mehrere Werte für Flags-Parameter sind ungültig.  <br/> |
|MAPI_E_DISK_ERROR  <br/> |Es wurde ein Problem beim Schreiben in oder Lesen vom Datenträger.  <br/> |
|MAPI_E_NOT_ENOUGH_DISK  <br/> |Es war nicht genügend Speicherplatz zum Abschließen des Vorgangs verfügbar.  <br/> |
|MAPI_E_NOT_ENOUGH_MEMORY  <br/> |Es ist nicht genügend Arbeitsspeicher verfügbar, um den Vorgang abzuschließen.  <br/> |
|MAPI_E_NOT_ENOUGH_RESOURCES  <br/> |Nicht genügend Systemressourcen waren zum Abschließen des Vorgangs verfügbar.  <br/> |
|MAPI_E_BAD_CHARWIDTH  <br/> |Eine Inkompatibilität vorhanden ist, in die Zeichensätze, die von dem Anrufer und der Implementierung unterstützt werden.  <br/> |
|MAPI_E_CALL_FAILED  <br/> |Unerwarteter oder unbekannten Ursprungs ein Fehler aufgetreten.  <br/> |
   
Die Konstanten, die MAPI-Rückgabewerte darstellen, sind in der MAPICODE aufgeführt. H-Headerdatei. Einige der Konstanten zuordnen zu Win32-Fehler; die Zuordnung der folgenden Konstanten für numerische Werte kann in der Win32-Headerdatei WINERROR gefunden werden. H.
  
Fehler bezüglich ungültige Daten vom Anrufer übergebene können über entweder den Parameter Validierung API bereitgestellten Funktionen MAPI oder eine Gruppe von Makros ermittelt werden. 
  
Character Set Inkompatibilität tritt auf, wenn eine der folgenden Situationen auftritt:
  
- Ein Client oder Dienstanbieter legt die Option MAPI_UNICODE bei einem Aufruf-Methode oder die Funktion, und die Implementierung Unicode nicht unterstützt. Festlegen von Parameter MAPI_UNICODE gibt an, dass Zeichenfolgen, die als Eingabe übergebenen Unicode-Zeichenfolgen und Zeichenfolgen übergeben wieder als Ausgabe erwartet werden Unicode-Zeichenfolgen.
    
- Ein Client oder Dienstanbieter wird die Option MAPI_UNICODE ein Gespräch über eine Methode oder Funktion nicht festgelegt, und die Implementierung unterstützt nur Unicode.
    

