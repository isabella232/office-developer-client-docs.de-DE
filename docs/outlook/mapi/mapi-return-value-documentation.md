---
title: MAPI-Rückgabewertdokumentation
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: c32ee53c-b063-4a00-a6bf-75ce5e07f56a
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 8c746b85716af43ac5a65be62d087822a88d5482
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59610195"
---
# <a name="mapi-return-value-documentation"></a>MAPI-Rückgabewertdokumentation

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Die Referenzeinträge in diesem Referenzdokument geben nur die Werte zurück, die eine gewisse Verarbeitung durch Clientanwendungen erfordern. Rückgabewerte, die allgemeine Fehlerbedingungen angeben und durch Überprüfen auf Fehler abgeleitet werden können, sind in der Dokumentation nicht enthalten. Beispielsweise können viele Schnittstellenmethoden MAPI_E_INVALID_PARAMETER zurückgeben, wenn ein Aufrufer den falschen Wert für einen Eingabeparameter angibt. Dieser Wert wird in der Regel nicht in der Gruppe der erwarteten Rückgabewerte aufgeführt, da nicht speziell nach MAPI_E_INVALID_PARAMETER gesucht werden muss und er nicht anders als jeder andere Fehler verarbeitet werden muss. Andererseits unterstützen einige Dienstanbieter keine Ereignisbenachrichtigung und geben MAPI_E_NO_SUPPORT an die Von Clients über **IMAPISession** **vorgenommene Advise-Methode** zurück. Da Clients explizit nach diesem Wert suchen und Code für die Behandlung der Bedingung bereitstellen müssen, die sie darstellt, sollte sie auftreten, ist MAPI_E_NO_SUPPORT in der Liste der Rückgabewerte für [IMAPISession::Advise](imapisession-advise.md)enthalten.
  
In der folgenden Tabelle werden Fehlerwerte beschrieben, die häufig von Methoden und Funktionen zurückgegeben werden und eine explizite Behandlung durch einen Client oder Dienstanbieter erfordern. Diese Werte werden in vier Kategorien unterteilt: Werte, die auf ungültige Eingabedaten hinweisen, Werte, die auf Ressourcenprobleme hinweisen, Werte, die auf Inkompatibilität von Zeichengruppen hinweisen, und Werte, die auf fehler eines unbekannten Ursprungs hinweisen.
  
|**Rückgabewert**|**Beschreibung**|
|:-----|:-----|
|MAPI_E_INVALID_PARAMETER  <br/> |Mindestens einer der an die Methode oder Funktionen übergebenen Parameter war ungültig.  <br/> |
|MAPI_E_UNKNOWN_FLAGS  <br/> |Mindestens ein Wert für einen Flags-Parameter war ungültig.  <br/> |
|MAPI_E_DISK_ERROR  <br/> |Es ist ein Problem beim Schreiben auf oder beim Lesen vom Datenträger aufgetreten.  <br/> |
|MAPI_E_NOT_ENOUGH_DISK  <br/> |Es war nicht genügend Speicherplatz verfügbar, um den Vorgang abzuschließen.  <br/> |
|MAPI_E_NOT_ENOUGH_MEMORY  <br/> |Es war nicht genügend Arbeitsspeicher verfügbar, um den Vorgang abzuschließen.  <br/> |
|MAPI_E_NOT_ENOUGH_RESOURCES  <br/> |Es waren nicht genügend Systemressourcen verfügbar, um den Vorgang abzuschließen.  <br/> |
|MAPI_E_BAD_CHARWIDTH  <br/> |In den Zeichensätzen, die vom Aufrufer und der Implementierung unterstützt werden, ist eine Inkompatibilität vorhanden.  <br/> |
|MAPI_E_CALL_FAILED  <br/> |Ein Fehler mit unerwartetem oder unbekanntem Ursprung ist aufgetreten.  <br/> |
   
Die Konstanten, die MAPI-Rückgabewerte darstellen, sind im MAPICODE aufgeführt. H-Headerdatei. Einige der Konstanten werden Win32-Fehlern zugeordnet. Die Zuordnung dieser Konstanten zu numerischen Werten finden Sie in der Win32-Headerdatei WINERROR.H.
  
Fehler in Bezug auf ungültige Daten, die von einem Aufrufer übergeben werden, können entweder über die von der MAPI bereitgestellten Parameterüberprüfungs-API-Funktionen oder eine Reihe von Makros bestimmt werden. 
  
Die Inkompatibilität des Zeichensatzes tritt auf, wenn eine der folgenden Situationen auftritt:
  
- Ein Client oder Dienstanbieter legt das MAPI_UNICODE Flag für einen Methoden- oder Funktionsaufruf fest, und die Implementierung unterstützt unicode nicht. Das Festlegen MAPI_UNICODE gibt an, dass als Eingabe übergebene Zeichenzeichenfolgen Unicode-Zeichenfolgen sind und dass als Ausgabe übergebene Zeichenzeichenfolgen Unicode-Zeichenfolgen sein sollen.
    
- Ein Client oder Dienstanbieter legt das MAPI_UNICODE Flag für einen Methoden- oder Funktionsaufruf nicht fest, und die Implementierung unterstützt nur Unicode.
    

