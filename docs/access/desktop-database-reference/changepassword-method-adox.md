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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32296528"
---
# <a name="changepassword-method-adox"></a>ChangePassword-Methode (ADOX)

**Gilt für**: Access 2013, Office 2013

Ändert das Kennwort für ein Benutzerkonto.

## <a name="syntax"></a>Syntax

*Benutzer*. ChangePassword*oldPassword*, *Neues Kennwort*

## <a name="parameters"></a>Parameter

|Parameter|Beschreibung|
|:--------|:----------|
|*OldPassword* |Ein **String**-Wert, der das aktuelle Kennwort des Benutzers angibt. Wenn der Benutzer aktuell über kein Kennwort verfügt, verwenden Sie für *OldPassword* eine leere Zeichenfolge ("").|
|*NewPassword* |Ein **String**-Wert, der das neue Kennwort angibt.|

## <a name="remarks"></a>Bemerkungen

Aus Sicherheitsgründen muss das alte Kennwort zusätzlich zum neuen Kennwort angegeben werden.

Wenn der Anbieter die Verwaltung von Vertrauensnehmereigenschaften nicht unterstützt, tritt ein Fehler auf.

