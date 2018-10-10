---
title: ChangePassword-Methode (ADOX)
TOCTitle: ChangePassword Method (ADOX)
ms:assetid: 999826a5-3e6b-b6da-b8f6-d61b9a50ceca
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249690(v=office.15)
ms:contentKeyID: 48546519
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 2bd2f5d87c6f90e940858ce5c6e01099c5e539d4
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25472985"
---
# <a name="changepassword-method-adox"></a>ChangePassword-Methode (ADOX)


**Betrifft**: Access 2013 | Office 2013



Ändert das Kennwort für ein Benutzerkonto.

## <a name="syntax"></a>Syntax

*Benutzer*. ChangePassword*AltesKennwort*, *NewPassword*

## <a name="parameters"></a>Parameters

  - *AltesKennwort*

  - Ein **String**-Wert, der das aktuelle Kennwort des Benutzers angibt. Wenn der Benutzer aktuell über kein Kennwort verfügt, verwenden Sie für *OldPassword* eine leere Zeichenfolge ("").

  - *NewPassword*

  - Ein **String** -Wert, der das neue Kennwort angibt.

## <a name="remarks"></a>Hinweise

Aus Sicherheitsgründen muss das alte Kennwort zusätzlich zum neuen Kennwort angegeben werden.

Wenn der Anbieter die Verwaltung von Vertrauensnehmereigenschaften nicht unterstützt, tritt ein Fehler auf.

