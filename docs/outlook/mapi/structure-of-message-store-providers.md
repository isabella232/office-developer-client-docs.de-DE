---
title: Struktur eines Nachrichtenspeicheranbieters
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 064b2fc1-e690-43e6-95d3-a61438115de5
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: d2b6c11453ccbb127c684ccde7773bc09c1f7a49
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59578557"
---
# <a name="structure-of-message-store-providers"></a>Struktur eines Nachrichtenspeicheranbieters
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Ein Nachrichtenspeicheranbieter ist, wenn er im Arbeitsspeicher ausgeführt wird, eine [IMSProvider : IUnknown-Schnittstelle.](imsprovideriunknown.md) Die **IMSProvider-Schnittstelle** ermöglicht Clientanwendungen und dem MAPI-Spooler die Anmeldung am und vom Nachrichtenspeicher. Die Schnittstellen, die Clientanwendungen und der MAPI-Spooler für den Zugriff auf Ordner und Nachrichten im Nachrichtenspeicher verwenden, sind [IMSLogon-](imslogoniunknown.md) und [IMsgStore-Schnittstellen.](imsgstoreimapiprop.md) Diese Schnittstellen werden in der Regel erstellt, wenn der Nachrichtenspeicher zum ersten Mal angemeldet ist, obwohl sie auch vom [MSProviderInit-Einstiegspunkt](msproviderinit.md) der Nachrichtenspeicher-DLL erstellt werden können. 
  
Da die **IMSLogon-** und **IMsgStore-Schnittstellen** einige Methoden gemeinsam verwenden, ist es möglicherweise einfacher, ein Klassenobjekt zu erstellen, das von beiden Schnittstellen erbt. Sie können diese Schnittstellen auch in separaten Objekten implementieren und interne Hilfsfunktionen in Die DLL schreiben, die die freigegebenen Methoden implementieren, die dann von den Methoden in den **IMSLogon-** und **IMsgStore-Schnittstellen** aufgerufen werden können. 
  
Die folgende Abbildung zeigt eine allgemeine Gliederung der Objekthierarchie innerhalb eines ausgeführten Nachrichtenspeichers.
  
**Objekthierarchie des Nachrichtenspeichers**
  
![Objekthierarchie des Nachrichtenspeichers](media/storeobj.gif "Objekthierarchie des Nachrichtenspeichers")
  
## <a name="see-also"></a>Siehe auch

- [Entwickeln eines MAPI-Nachrichtenspeicheranbieters](developing-a-mapi-message-store-provider.md)

