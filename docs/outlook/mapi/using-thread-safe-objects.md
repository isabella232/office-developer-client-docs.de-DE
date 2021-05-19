---
title: Verwenden Thread-Safe Objekten
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: e688db5e-d1a1-4afc-998f-b3d31eb6239b
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 611e0a49f0fd8df8fe40205a33ed5501055c3d45
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425169"
---
# <a name="using-thread-safe-objects"></a>Verwenden Thread-Safe Objekten

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Clientanwendungen können davon ausgehen, dass objekte, die direkt oder als Rückrufe verwendet werden, immer threadsicher sind, außer in den folgenden Fällen:
  
- Das Statusobjekt eines Transportanbieters, das über einen Clientaufruf von [IMAPISession::OpenEntry](imapisession-openentry.md) mit einem Eintragsbezeichner aus der Statustabelle des Anbieters erhalten wurde. 
    
- Alle MAPI-Formularobjekte, die über einen Clientaufruf von [MAPIOpenFormMgr erhalten wurden.](mapiopenformmgr.md) Formularobjekte befolgen Apartmentmodellregeln, und Clients müssen sie und alle darin enthaltenen Objekte nur im Thread verwenden, von dem sie erstellt wurden.
    
Wenn ein Client auf die Zeile eines Transportanbieters in der Statustabelle zutritt, die die Eintrags-ID des zugeordneten Statusobjekts enthält, kann der Client **OpenEntry** mit diesem Eintragsbezeichner aufrufen, um das Statusobjekt zu öffnen. Dieses Statusobjekt ist nicht threadsicher, da Transportanbieter im Kontext des MAPI-Spoolers ausgeführt werden und keinen separaten Kontext für ihr Statusobjekt beibehalten. Das status-Objekt befolgt Apartmentmodellregeln, und Clients dürfen es nur für den Thread verwenden, von dem es erstellt wurde. 
  
Ein Client muss [mapIInitialize](mapiinitialize.md) auch in jedem Thread aufrufen, bevor mapI-Objekte verwendet werden und [MAPIUninitialize,](mapiuninitialize.md) wenn diese Verwendung abgeschlossen ist. Diese Aufrufe sollten auch dann ausgeführt werden, wenn die zu verwendenden Objekte von einer externen Quelle an den Thread übergeben werden. **MAPIInitialize** und **MAPIUninitialize** können von überall aufgerufen werden, mit Ausnahme einer Win32 **DllMain-Funktion,** einer Funktion, die vom System aufgerufen wird, wenn Prozesse und Threads initialisiert und beendet werden, oder bei Aufrufen der **LoadLibrary-** und **FreeLibrary-Funktionen.** 
  
Indirekte Verwendungsobjekte sollten niemals als threadsicher angenommen werden. Indirekte Verwendungsobjekte werden von Methoden zurückgegeben, für die Zielschnittstellenzeiger als Eingabeparameter erforderlich sind. Beispiele für solche Methoden sind **IMAPIProp::CopyTo** und **CopyProps**, **IMAPIFolder::CopyFolder** und **CopyMessage** und **IMsgServiceAdmin::CopyMsgService**. Wenn ein Dienstanbieter ein solches Objekt von einem anderen Thread als dem Thread aufrufen möchte, an den es übergeben wurde, ist der Anbieter für das explizite Marshalling des Objekts verantwortlich.
  

