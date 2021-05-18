---
title: PROP_ACCT_PREFERENCES_UID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: ec0aac33-624e-48f7-8177-8f7b8db6af7d
description: Ruft den eindeutigen Bezeichner (Unique Identifier, UID) für den Profilabschnitt ab, in dem die Kontoeinstellungen gespeichert sind.
ms.openlocfilehash: 97f1a858c8f58e13b72b8d5f052b35359581b718
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327636"
---
# <a name="prop_acct_preferences_uid"></a>PROP_ACCT_PREFERENCES_UID

Ruft den eindeutigen Bezeichner (Unique Identifier, UID) für den Profilabschnitt ab, in dem die Kontoeinstellungen gespeichert sind. 
  
## <a name="quick-info"></a>QuickInfo

Siehe [IOlkAccount](iolkaccount.md).
  
|||
|:-----|:-----|
|Kennung:  <br/> |0x0022  <br/> |
|Eigenschaftstyp:  <br/> |PT_BINARY  <br/> |
|Eigenschaftstag:  <br/> |0x00220102  <br/> |
|Zugriff:  <br/> |Schreibgeschützt  <br/> |
   
## <a name="remarks"></a>Hinweise

Verwenden **PROP_ACCT_PREFERENCES_UID** in Aufrufen von [IMAPISupport::OpenProfileSection,](https://msdn.microsoft.com/library/cd1fa994-9531-46c4-94e5-505e7f90b884%28Office.15%29.aspx) um den Profilabschnitt abzurufen, der Kontoeinstellungen enthält. 
  
## <a name="see-also"></a>Siehe auch

- [Über die Konto-API](about-the-account-management-api.md)
- [Anti-Spam-Einstellungen](about-anti-spam-settings.md)

