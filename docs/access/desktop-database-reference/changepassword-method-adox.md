---
title: ChangePassword-Methode (ADOX)
TOCTitle: ChangePassword method (ADOX)
ms:assetid: 999826a5-3e6b-b6da-b8f6-d61b9a50ceca
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249690(v=office.15)
ms:contentKeyID: 48546519
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 5fdc08b191e735ddcad0b9dae9962cb657521993
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59590093"
---
# <a name="changepassword-method-adox"></a>ChangePassword-Methode (ADOX)

**Gilt für**: Access 2013, Office 2013

Ändert das Kennwort für ein Benutzerkonto.

## <a name="syntax"></a>Syntax

*Benutzer*. ChangePassword *OldPassword*, *NewPassword*

## <a name="parameters"></a>Parameter

|Parameter|Beschreibung|
|:--------|:----------|
|*Oldpassword* |Ein **String**-Wert, der das aktuelle Kennwort des Benutzers angibt. Wenn der Benutzer aktuell über kein Kennwort verfügt, verwenden Sie für *OldPassword* eine leere Zeichenfolge ("").|
|*Newpassword* |Ein **String**-Wert, der das neue Kennwort angibt.|

## <a name="remarks"></a>HinwBemerkungeneise

Aus Sicherheitsgründen muss das alte Kennwort zusätzlich zum neuen Kennwort angegeben werden.

Wenn der Anbieter die Verwaltung von Vertrauensnehmereigenschaften nicht unterstützt, tritt ein Fehler auf.

