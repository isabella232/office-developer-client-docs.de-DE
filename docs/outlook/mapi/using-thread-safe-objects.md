---
title: Verwenden von Thread sicheren Objekten
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: e688db5e-d1a1-4afc-998f-b3d31eb6239b
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 611e0a49f0fd8df8fe40205a33ed5501055c3d45
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329589"
---
# <a name="using-thread-safe-objects"></a>Verwenden von Thread sicheren Objekten

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Client Anwendungen können davon ausgehen, dass Objekte, die direkt oder als Rückrufe verwendet werden, nur in den folgenden Fällen threadsicher sind:
  
- Das Statusobjekt eines Transportanbieters, das über einen Clientaufruf von [IMAPISession:: OpenEntry](imapisession-openentry.md) mit einer Eintrags-ID aus der Statustabellen Zeile des Anbieters abgerufen wurde. 
    
- Alle MAPI-Formularobjekte, die über einen Clientaufruf an [MAPIOpenFormMgr](mapiopenformmgr.md)abgerufen werden. Formularobjekte gehorchen Apartmentmodell Regeln, und Clients müssen diese und alle darin enthaltenen Objekte nur für den Thread verwenden, der Sie erstellt hat.
    
Wenn ein Client in der Statustabelle, die die Eintrags-ID des zugeordneten Status Objekts enthält, auf die Zeile eines Transportanbieters zugreift **** , kann der Client OpenEntry mit dieser Eintrags-ID aufrufen, um das Status-Objekt zu öffnen. Dieses Statusobjekt ist nicht threadsicher, da Transportanbieter im Kontext des MAPI-Spoolers ausgeführt werden und keinen separaten Kontext für Ihr Status-Objekt beibehalten. Das Status-Objekt befolgt Apartmentmodell Regeln, und Clients müssen es nur für den Thread verwenden, der es erstellt hat. 
  
Ein Client muss [MAPIInitialize](mapiinitialize.md) auch für jeden Thread aufrufen, bevor MAPI-Objekte und [MAPIUninitialize](mapiuninitialize.md) verwendet werden, wenn die Verwendung abgeschlossen ist. Diese Aufrufe sollten auch dann vorgenommen werden, wenn die zu verwendenden Objekte aus einer externen Quelle an den Thread übergeben werden. **MAPIInitialize** und **MAPIUninitialize** können von überall aus aufgerufen werden, außer innerhalb einer Win32- **DllMain** -Funktion, eine Funktion, die vom System aufgerufen wird, wenn Prozesse und Threads initialisiert und beendet werden, oder bei Aufrufen der ** LoadLibrary** -und **FreeLibrary** -Funktionen. 
  
InDirekte use-Objekte sollten nie als threadsicher angenommen werden. InDirekte use-Objekte werden von Methoden zurückgegeben, die Ziel Schnittstellenzeiger als Eingabeparameter erfordern. Beispiele für solche Methoden sind **IMAPIProp:: CopyTo** und **CopyProps**, **IMAPIFolder:: CopyFolder** und **CopyMessage**und **IMsgServiceAdmin:: CopyMsgService**. Wenn ein Dienstanbieter ein solches Objekt aus einem anderen Thread als dem, an dem es übergeben wurde, aufrufen möchte, ist er dafür verantwortlich, das Objekt explizit zu marshallen.
  

