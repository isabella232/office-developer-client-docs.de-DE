---
title: ChangePassword-Methode (ADOX)
TOCTitle: ChangePassword method (ADOX)
ms:assetid: 999826a5-3e6b-b6da-b8f6-d61b9a50ceca
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249690(v=office.15)
ms:contentKeyID: 48546519
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: df67774b9b38b5fbcc836a2ea0dfc17886d67107
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28713093"
---
# <a name="changepassword-method-adox"></a>ChangePassword-Methode (ADOX)

**Betrifft**: Access 2013, Office 2013

Ändert das Kennwort für ein Benutzerkonto.

## <a name="syntax"></a>Syntax

*Benutzer*. ChangePassword*AltesKennwort*, *NewPassword*

## <a name="parameters"></a>Parameter

|Parameter|Beschreibung|
|:--------|:----------|
|*AltesKennwort* |Ein **String**-Wert, der das aktuelle Kennwort des Benutzers angibt. Wenn der Benutzer aktuell über kein Kennwort verfügt, verwenden Sie für *OldPassword* eine leere Zeichenfolge ("").|
|*NewPassword* |Ein **String** -Wert, der das neue Kennwort angibt.|

## <a name="remarks"></a>Hinweise

Aus Sicherheitsgründen muss das alte Kennwort zusätzlich zum neuen Kennwort angegeben werden.

Wenn der Anbieter die Verwaltung von Vertrauensnehmereigenschaften nicht unterstützt, tritt ein Fehler auf.

