---
title: MAPI-Rückgabewert Dokumentation
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: c32ee53c-b063-4a00-a6bf-75ce5e07f56a
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 5bbafe9fda479d951bb20175ab904dc6e241226a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329715"
---
# <a name="mapi-return-value-documentation"></a>MAPI-Rückgabewert Dokumentation

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Die Referenz Einträge in dieser Referenz dokumentieren nur die Rückgabewerte, die von Clientanwendungen verarbeitet werden müssen. Rückgabewerte, die häufige Fehlerbedingungen angeben und durch Überprüfen auf Fehler abgeleitet werden können, sind in der Dokumentation nicht enthalten. Viele Schnittstellenmethoden können beispielsweise MAPI_E_INVALID_PARAMETER zurückgeben, wenn ein Aufrufer den falschen Wert für einen Eingabe Parameter angibt. Dieser Wert ist in der Regel nicht in der Gruppe der erwarteten Rückgabewerte aufgeführt, da es nicht erforderlich ist, speziell nach MAPI_E_INVALID_PARAMETER zu suchen, und es nicht erforderlich ist, es anders zu verarbeiten als andere Fehler. Andererseits unterstützen einige Dienstanbieter keine Ereignisbenachrichtigung und geben MAPI_E_NO_SUPPORT an die **Advise** -Methode zurück, die von Clients über **IMAPISession**durchgeführt wird. Da Clients diesen Wert explizit überprüfen und Code zur Behandlung der Bedingung bereitstellen müssen, die er darstellt, wenn er eintritt, ist MAPI_E_NO_SUPPORT in der Liste der Rückgabewerte für [IMAPISession:: Advise](imapisession-advise.md)enthalten.
  
In der folgenden Tabelle werden Fehlerwerte beschrieben, die häufig von Methoden und Funktionen zurückgegeben werden und eine explizite Behandlung durch einen Client oder Dienstanbieter erfordern. Diese Werte werden in vier Kategorien unterteilt: Werte, die ungültige Eingabedaten, Werte, die Ressourcenprobleme anzeigen, Werte, die die Inkompatibilität von Zeichensätzen anzeigen, und Werte, die den Fehler eines unbekannten Ursprungs kennzeichnen.
  
|**Rückgabewert**|**Beschreibung**|
|:-----|:-----|
|MAPI_E_INVALID_PARAMETER  <br/> |Mindestens einer der an die Methode oder Funktionen übergebenen Parameter war ungültig.  <br/> |
|MAPI_E_UNKNOWN_FLAGS  <br/> |Mindestens ein Wert für einen Flags-Parameter war ungültig.  <br/> |
|MAPI_E_DISK_ERROR  <br/> |Beim Schreiben oder Lesen vom Datenträger ist ein Problem aufgetreten.  <br/> |
|MAPI_E_NOT_ENOUGH_DISK  <br/> |Es war nicht genügend Speicherplatz verfügbar, um den Vorgang abzuschließen.  <br/> |
|MAPI_E_NOT_ENOUGH_MEMORY  <br/> |Es war nicht genügend Arbeitsspeicher verfügbar, um den Vorgang abzuschließen.  <br/> |
|MAPI_E_NOT_ENOUGH_RESOURCES  <br/> |Es waren nicht genügend Systemressourcen verfügbar, um den Vorgang abzuschließen.  <br/> |
|MAPI_E_BAD_CHARWIDTH  <br/> |Eine Inkompatibilität besteht in den Zeichensätzen, die vom Aufrufer und der Implementierung unterstützt werden.  <br/> |
|MAPI_E_CALL_FAILED  <br/> |Ein Fehler unerwarteter oder unbekannter Herkunft ist aufgetreten.  <br/> |
   
Die Konstanten, die MAPI-Rückgabewerte darstellen, werden im MAPICODE aufgelistet. H-Headerdatei. Einige der Konstanten werden Win32-Fehlern zugeordnet. die Zuordnung dieser Konstanten zu numerischen Werten finden Sie in der Win32-Headerdatei WINERROR. H.
  
Fehler in Bezug auf ungültige Daten, die von einem Aufrufer übergeben wurden, können entweder über die von MAPI bereitgestellten API-Funktionen für die Parametervalidierung oder eine Gruppe von Makros bestimmt werden. 
  
Die Inkompatibilität von Zeichensätzen tritt auf, wenn eine der folgenden Situationen eintritt:
  
- Ein Client oder Dienstanbieter legt das MAPI_UNICODE-Flag für eine Methode oder einen Funktionsaufruf fest, und die Implementierung unterstützt Unicode nicht. Setting MAPI_UNICODE gibt an, dass Zeichen Zeichenfolgen, die als Eingabe übergeben werden, Unicode-Zeichenfolgen sind und dass Zeichen Zeichenfolgen, die als Ausgabe zurückgegeben werden, als Unicode-Zeichenfolgen erwartet werden.
    
- Ein Client oder Dienstanbieter legt das MAPI_UNICODE-Flag für eine Methode oder einen Funktionsaufruf nicht fest, und die Implementierung unterstützt nur Unicode.
    

