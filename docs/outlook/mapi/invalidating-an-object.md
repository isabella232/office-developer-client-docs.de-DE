---
title: Unwirksammachen eines Objekts
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 7d601cee-ffc4-4c7c-8006-40b717dee247
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 2346ec8541e1a8b7f5ea198722833447f9f5a289
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22566474"
---
# <a name="invalidating-an-object"></a>Unwirksammachen eines Objekts

  
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
Als Teil des Herunterfahrens des Anbieters sollten Sie ein Objekt ungültig. Ein Objekt ungültig umfasst, und Ersetzen Sie die vtable des Objekts durch eine Vtable, die Implementierungen für die drei **IUnknown** -Methoden enthält: **QueryInterface**, **AddRef**und **Release**. Ein Objekt ungültig wird durch Aufrufen von [IMAPISupport::MakeInvalid](imapisupport-makeinvalid.md), eine Methode, die im jedes der drei allgemeine Providertypen Support-Objekt enthalten ist. Anbieter stellen dieses Anrufs in der Regel in der Implementierung von ihrer Anmeldung-Objekt **Logoff (** Methode). 
  
Ein Objekt ungültig bietet MAPI die ultimative Verantwortung für ein Objekt zugeordneten Arbeitsspeicher freizugeben. Sie können alle Ressourcen verbunden mit einem Objekt frei, und rufen Sie dann **MakeInvalid** , um alle Methoden in seiner geerbten Schnittstellen ungültig. Anrufe an eine der folgenden Methoden gibt MAPI_E_INVALID_OBJECT zurück. Verwenden von **MakeInvalid** ist eine Option, die viele Dienstanbieter ignoriert werden sollen. 
  
## <a name="see-also"></a>Siehe auch



[Herunterfahren eines Dienstanbieters](shutting-down-a-service-provider.md)

