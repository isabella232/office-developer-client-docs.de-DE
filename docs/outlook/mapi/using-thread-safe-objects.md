---
title: Verwenden von threadsicheren Objekten
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: e688db5e-d1a1-4afc-998f-b3d31eb6239b
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 49a94b785a51b4b0c3082832145250eec0745a19
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22580978"
---
# <a name="using-thread-safe-objects"></a>Verwenden von threadsicheren Objekten

  
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
Clientanwendungen können davon ausgehen, dass Objekte direkt verwendet oder als Rückrufe immer threadsicheren außer in den folgenden Fällen sind:
  
- Eines Transportdienstes-Objekt, der durch einen Clientaufruf von [IMAPISession::OpenEntry](imapisession-openentry.md) mit einem Eintrag Bezeichner aus der Anbieter Status Tabellenzeile abgerufen. 
    
- Alle MAPI-Formular-Objekten, die durch einen Clientaufruf [MAPIOpenFormMgr](mapiopenformmgr.md). Formular-Objekte gelten des Apartmentthreading Model Regeln und Clients müssen sie und alle Objekte, die von ihnen enthalten sind, nur in dem Thread, die sie erstellt hat.
    
Wenn ein Client eines Transportdienstes Zeile in der Tabelle "Status", die die Eintrags-ID des zugeordneten Status-Objekts enthält zugreift, kann der Client **OpenEntry** mit dieses Eintrags-ID zum Öffnen des Status-Objekts aufrufen. In diesem Statusobjekt ist nicht threadsicheren, da Transportanbieter im Zusammenhang mit der MAPI-Warteschlange ausführen und einen separaten Kontext für ihren Statusobjekt nicht beibehalten. Das Statusobjekt des Apartmentthreading Model Regeln erfüllt und Clients müssen nur auf Threads, der es erstellt. 
  
Ein Client muss auch ["MAPIInitialize"](mapiinitialize.md) auf jedem Thread aufrufen, um vor der Nutzung jeglicher MAPI-Objekten und [MAPIUninitialize](mapiuninitialize.md) nach Abschluss der, die verwenden. Diese Aufrufe erfolgen soll, auch wenn die Objekte, die verwendet werden, an der Thread aus einer externen Quelle übergeben werden. **"MAPIInitialize"** und **MAPIUninitialize** kann aus an einer beliebigen Stelle mit Ausnahme von innerhalb einer Win32 **DllMain** -Funktion eine Funktion aufgerufen werden, die vom System beim Prozesse und Threads initialisiert und beendet sind oder beim Aufrufen der **aufgerufen wird LoadLibrary** und **FreeLibrary** Funktionen. 
  
Indirekte Verwenden von Objekten sollte niemals Threadsicherheit vorgegeben werden. Indirekte Verwenden von Objekten werden von Methoden zurückgegeben, die Ziel-Schnittstellenzeiger als Eingabeparameter benötigen. Beispiele für solche Methoden sind **IMAPIProp::CopyTo** und **CopyProps**, **IMAPIFolder::CopyFolder** und **CopyMessage**und **IMsgServiceAdmin::CopyMsgService**. Wenn ein Dienstanbieter solches Objekt von einem Thread aufrufen als den, auf dem es übergeben wurde möchte, ist der Anbieter für das Objekt explizit Marshallen verantwortlich.
  

