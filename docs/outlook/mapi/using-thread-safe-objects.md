---
title: Verwenden von Thread-Safe-Objekten
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: e688db5e-d1a1-4afc-998f-b3d31eb6239b
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 418eb34ee6b66a941a32bc3e4dd7af29965d32c1
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59590884"
---
# <a name="using-thread-safe-objects"></a>Verwenden von Thread-Safe-Objekten

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Clientanwendungen können davon ausgehen, dass Objekte, die direkt oder als Rückrufe verwendet werden, immer threadsicher sind, außer in den folgenden Fällen:
  
- Das Statusobjekt eines Transportanbieters, das über einen Clientaufruf an [IMAPISession::OpenEntry](imapisession-openentry.md) mit einem Eintragsbezeichner aus der Statustabellenzeile des Anbieters abgerufen wurde. 
    
- Alle MAPI-Formularobjekte, die über einen Clientaufruf an [MAPIOpenFormMgr](mapiopenformmgr.md)abgerufen werden. Formularobjekte befolgen Apartmentmodellregeln, und Clients müssen sie und alle darin enthaltenen Objekte nur in dem Thread verwenden, der sie erstellt hat.
    
Wenn ein Client auf die Zeile eines Transportanbieters in der Statustabelle zugreift, die den Eintragsbezeichner des zugeordneten Statusobjekts enthält, kann der Client **OpenEntry** mit diesem Eintragsbezeichner aufrufen, um das Statusobjekt zu öffnen. Dieses Statusobjekt ist nicht threadsicher, da Transportanbieter im Kontext des MAPI-Spoolers ausgeführt werden und keinen separaten Kontext für ihr Statusobjekt verwalten. Das Statusobjekt entspricht Apartmentmodellregeln, und Clients dürfen es nur in dem Thread verwenden, der es erstellt hat. 
  
Ein Client muss [auch MAPIInitialize](mapiinitialize.md) in jedem Thread aufrufen, bevor MAPI-Objekte und [MAPIUninitialize](mapiuninitialize.md) verwendet werden, wenn diese Verwendung abgeschlossen ist. Diese Aufrufe sollten auch dann ausgeführt werden, wenn die zu verwendenden Objekte von einer externen Quelle an den Thread übergeben werden. **MAPIInitialize** und **MAPIUninitialize** können von überall aufgerufen werden, außer von innerhalb einer Win32 **DllMain-Funktion,** einer Funktion, die vom System aufgerufen wird, wenn Prozesse und Threads initialisiert und beendet werden, oder bei Aufrufen der **Funktionen LoadLibrary** und **FreeLibrary.** 
  
Indirekte Verwendungsobjekte sollten niemals threadsicher sein. Indirekte Verwendungsobjekte werden von Methoden zurückgegeben, die Zielschnittstellenzeiger als Eingabeparameter erfordern. Beispiele für solche Methoden sind **IMAPIProp::CopyTo** und **CopyProps**, **IMAPIFolder::CopyFolder** und **CopyMessage** und **IMsgServiceAdmin::CopyMsgService**. Wenn ein Dienstanbieter ein solches Objekt aus einem anderen Thread aufrufen möchte als dem Thread, an den es übergeben wurde, ist der Anbieter für das explizite Marshalling des Objekts verantwortlich.
  

