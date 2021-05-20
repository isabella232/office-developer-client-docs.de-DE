---
title: MAPI-Rückgabewertdokumentation
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: c32ee53c-b063-4a00-a6bf-75ce5e07f56a
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 5bbafe9fda479d951bb20175ab904dc6e241226a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33429691"
---
# <a name="mapi-return-value-documentation"></a>MAPI-Rückgabewertdokumentation

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Die Referenzeinträge in diesem Referenzdokument geben nur werte zurück, die eine gewisse Verarbeitung durch Clientanwendungen erfordern. Rückgabewerte, die allgemeine Fehlerbedingungen angeben und durch Überprüfung auf Fehler abgeleitet werden können, sind nicht in der Dokumentation enthalten. Beispielsweise können viele Schnittstellenmethoden MAPI_E_INVALID_PARAMETER, wenn ein Aufrufer den falschen Wert für einen Eingabeparameter angibt. Dieser Wert wird in der Regel nicht in der Gruppe der erwarteten Rückgabewerte aufgeführt, da es nicht nötig ist, speziell nach MAPI_E_INVALID_PARAMETER zu suchen und ihn nicht anders als bei anderen Fehlern zu verarbeiten. Andererseits unterstützen einige Dienstanbieter keine Ereignisbenachrichtigung und geben MAPI_E_NO_SUPPORT der **Advise-Methode** zurück, die von Clients über **IMAPISession vorgenommen wurde.** Da Clients explizit auf diesen Wert überprüfen und Code für die Behandlung der Bedingung bereitstellen müssen, die er im Fall des Auftretens darstellt, ist MAPI_E_NO_SUPPORT in der Liste der Rückgabewerte für [IMAPISession::Advise enthalten.](imapisession-advise.md)
  
In der folgenden Tabelle werden Fehlerwerte beschrieben, die häufig von Methoden und Funktionen zurückgegeben werden und eine explizite Behandlung durch einen Client oder Dienstanbieter erfordern. Diese Werte sind in vier Kategorien unterteilt: Werte, die ungültige Eingabedaten angeben, Werte, die Ressourcenprobleme angeben, Werte, die auf Inkompatibilität des Zeichensatzs hinweisen, und Werte, die auf einen Fehler eines unbekannten Ursprungs hinweisen.
  
|**Rückgabewert**|**Beschreibung**|
|:-----|:-----|
|MAPI_E_INVALID_PARAMETER  <br/> |Mindestens einer der an die Methode oder Funktionen übergebenen Parameter war ungültig.  <br/> |
|MAPI_E_UNKNOWN_FLAGS  <br/> |Mindestens ein Wert für einen Flags-Parameter war ungültig.  <br/> |
|MAPI_E_DISK_ERROR  <br/> |Es ist ein Problem beim Schreiben oder Lesen von Datenträgern vorhanden.  <br/> |
|MAPI_E_NOT_ENOUGH_DISK  <br/> |Es war nicht genügend Speicherplatz verfügbar, um den Vorgang abschließen zu können.  <br/> |
|MAPI_E_NOT_ENOUGH_MEMORY  <br/> |Es war nicht genügend Arbeitsspeicher verfügbar, um den Vorgang abschließen zu können.  <br/> |
|MAPI_E_NOT_ENOUGH_RESOURCES  <br/> |Es waren nicht genügend Systemressourcen verfügbar, um den Vorgang abschließen zu können.  <br/> |
|MAPI_E_BAD_CHARWIDTH  <br/> |In den vom Aufrufer und der Implementierung unterstützten Zeichensätzen ist eine Inkompatibilität vorhanden.  <br/> |
|MAPI_E_CALL_FAILED  <br/> |Ein Fehler mit unerwartetem oder unbekanntem Ursprung ist aufgetreten.  <br/> |
   
Die Konstanten, die MAPI-Rückgabewerte darstellen, sind im MAPICODE aufgeführt. H-Headerdatei. Einige der Konstanten werden Win32-Fehlern zuordnungen. Die Zuordnung dieser Konstanten zu numerischen Werten finden Sie in der Win32-Headerdatei WINERROR.H.
  
Fehler in Bezug auf ungültige Daten, die von einem Aufrufer übergeben werden, können entweder über die von MAPI bereitgestellten Parametervalidierungs-API-Funktionen oder eine Reihe von Makros ermittelt werden. 
  
Die Inkompatibilität von Zeichensatz tritt auf, wenn eine der folgenden Situationen auftritt:
  
- Ein Client oder Dienstanbieter legt das MAPI_UNICODE für einen Methoden- oder Funktionsaufruf fest, und die Implementierung unterstützt Unicode nicht. Das MAPI_UNICODE gibt an, dass zeichenzeichenfolgen, die als Eingabe übergeben werden, Unicode-Zeichenfolgen sind und zeichenzeichenfolgen, die als Ausgabe übergeben werden, als Unicode-Zeichenfolgen erwartet werden.
    
- Ein Client oder Dienstanbieter setzt das MAPI_UNICODE für einen Methoden- oder Funktionsaufruf nicht, und die Implementierung unterstützt nur Unicode.
    

