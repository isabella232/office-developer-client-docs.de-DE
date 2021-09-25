---
title: PROP_ACCT_PREFERENCES_UID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: ec0aac33-624e-48f7-8177-8f7b8db6af7d
description: Ruft den eindeutigen Bezeichner (UID) für den Profilabschnitt ab, in dem die Kontoeinstellungen gespeichert sind.
ms.openlocfilehash: 34c781f4a6a1692416f4a33b7cc34ebcf3375c9d
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59625637"
---
# <a name="prop_acct_preferences_uid"></a>PROP_ACCT_PREFERENCES_UID

Ruft den eindeutigen Bezeichner (UID) für den Profilabschnitt ab, in dem die Kontoeinstellungen gespeichert sind. 
  
## <a name="quick-info"></a>QuickInfo

Siehe [IOlkAccount](iolkaccount.md).
  
|||
|:-----|:-----|
|Kennung:  <br/> |0x0022  <br/> |
|Eigenschaftentyp:  <br/> |PT_BINARY  <br/> |
|Eigenschaftstag:  <br/> |0x00220102  <br/> |
|Zugriff:  <br/> |Schreibgeschützt  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Verwenden Sie **PROP_ACCT_PREFERENCES_UID** in Aufrufen von [IMAPISupport::OpenProfileSection,](https://msdn.microsoft.com/library/cd1fa994-9531-46c4-94e5-505e7f90b884%28Office.15%29.aspx) um den Profilabschnitt abzurufen, der Kontoeinstellungen enthält. 
  
## <a name="see-also"></a>Siehe auch

- [Über die Konto-API](about-the-account-management-api.md)
- [Anti-Spam-Einstellungen](about-anti-spam-settings.md)

