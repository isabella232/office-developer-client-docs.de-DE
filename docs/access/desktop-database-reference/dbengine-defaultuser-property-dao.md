---
title: DBEngine.DefaultUser-Eigenschaft (DAO)
TOCTitle: DefaultUser Property
ms:assetid: 41ee0211-0794-6026-7341-3698a0b2c588
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192905(v=office.15)
ms:contentKeyID: 48544464
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1053071
f1_categories:
- Office.Version=v15
ms.localizationpriority: medium
ms.openlocfilehash: 4b6a8a8f65b450d38a820bd00468cbde38facbd6
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59585816"
---
# <a name="dbenginedefaultuser-property-dao"></a>DBEngine.DefaultUser-Eigenschaft (DAO)


**Gilt für**: Access 2013, Office 2013

Legt den Benutzernamen fest, mit dem das Standardobjekt **Workspace** bei seiner Initialisierung erstellt wird. **String**-Wert mit Lese-/Schreibzugriff.

## <a name="syntax"></a>Syntax

*Ausdruck* . DefaultUser

*expression* Ein Ausdruck, der ein **DBEngine**-Objekt zurückgibt.

## <a name="remarks"></a>HinwBemerkungeneise

The setting for **DefaultUser** is a String data type. Sie kann in Microsoft Access-Arbeitsbereichen 1 bis 20 Zeichen lang sein und alphabetische Zeichen, Akzentzeichen, Zahlen, Leerzeichen und Symbole enthalten, außer für: " (Anführungszeichen), / (Schrägstrich), \\ (umgekehrter Schrägstrich), \[ \] (Klammern), : (Doppelpunkt), | (Pipe), \< (less-than sign), \> (Größer-als-Zeichen), + (Pluszeichen), = (Gleichheitszeichen), ; (Semikolon), , ( Komma), ? (Fragezeichen), \* (Sternchen), führende Leerzeichen und Steuerzeichen (ASCII 00 bis ASCII 31).


> [!NOTE]
> [!HINWEIS] Verwenden Sie sichere Kennwörter aus Groß- und Kleinbuchstaben, Zahlen und Symbolen. Unsichere Kennwörter enthalten keine Kombination dieser Elemente. Sicheres Kennwort: Y6dh!et5. Unsicheres Kennwort: Haus27. Verwenden Sie ein sicheres Kennwort, das Sie sich gut merken können, damit Sie es nicht aufschreiben müssen.

Die **DefaultUser**-Eigenschaft ist standardmäßig auf "admin" und die **DefaultPassword**-Eigenschaft auf eine leere Zeichenfolge ("") festgelegt.

Bei Benutzernamen wird die Groß-/Kleinschreibung in der Regel nicht beachtet. Wenn Sie jedoch ein Benutzerkonto erstellen, das gelöscht oder in einer anderen Arbeitsgruppe erstellt wurde, muss die Groß-/Kleinschreibung beim Benutzernamen genau mit der Schreibweise des ursprünglichen Namens übereinstimmen. Bei Kennwörtern wird die Groß-/Kleinschreibung beachtet.

In der Regel erstellen Sie mit der **CreateWorkspace**-Methode ein **Workspace**-Objekt mit einem bestimmten Benutzernamen und Kennwort. Aus Gründen der Abwärtskompatibilität mit früheren Versionen und zur Arbeitserleichterung, wenn Sie keine sichere Datenbank implementieren, erstellt das Microsoft Access-Datenbankmodul automatisch bei Bedarf ein **Workspace**-Standardobjekt, falls noch keines geöffnet ist. In diesem Fall definieren die Werte der Eigenschaften **DefaultUser** und **DefaultPassword** den Benutzer und das Kennwort für das **Workspace**-Standardobjekt.

Damit diese Eigenschaft wirksam wird, müssen Sie sie festlegen, bevor Sie eine der DAO-Methoden aufrufen.

