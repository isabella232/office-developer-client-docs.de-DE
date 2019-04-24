---
title: DbEngine. DefaultUser-Eigenschaft (DAO)
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
localization_priority: Normal
ms.openlocfilehash: c29f9663ce3591fe5b1633239e8ec0d8866ee16a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32294346"
---
# <a name="dbenginedefaultuser-property-dao"></a>DbEngine. DefaultUser-Eigenschaft (DAO)


**Gilt für**: Access 2013, Office 2013

Legt den Benutzernamen fest, mit dem das Standardobjekt **Workspace** bei seiner Initialisierung erstellt wird. **String**-Wert mit Lese-/Schreibzugriff.

## <a name="syntax"></a>Syntax

*Ausdruck* . DefaultUser

*Ausdruck* Ein Ausdruck, der ein **DBEngine** -Objekt zurückgibt.

## <a name="remarks"></a>Bemerkungen

The setting for **DefaultUser** is a String data type. Es kann 1 bis 20 Zeichen lang in Microsoft Access-Arbeitsbereichen, und es kann alphabetische Zeichen, Akzentzeichen, Zahlen, Leerzeichen und Symbole enthalten, mit Ausnahme von: "(Anführungszeichen),/( \\ Schrägstrich), \[ \] (Backslash), (Klammern) ,: (Doppelpunkt), | (Pipe), \< (kleiner-als-Zeichen) \> , (größer-als-Zeichen), + (Pluszeichen), = (Gleichheitszeichen),; (Semikolon),, (Komma),? (Fragezeichen), \* (Asterisk), führende Leerzeichen und Steuerelemente (ASCII 00 bis ASCII 31).


> [!NOTE]
> [!HINWEIS] Verwenden Sie sichere Kennwörter aus Groß- und Kleinbuchstaben, Zahlen und Symbolen. Unsichere Kennwörter enthalten keine Kombination dieser Elemente. Sicheres Kennwort: Y6dh!et5. Unsicheres Kennwort: Haus27. Verwenden Sie ein sicheres Kennwort, das Sie sich gut merken können, damit Sie es nicht aufschreiben müssen.

Die **DefaultUser**-Eigenschaft ist standardmäßig auf "admin" und die **DefaultPassword**-Eigenschaft auf eine leere Zeichenfolge ("") festgelegt.

Bei Benutzernamen wird die Groß-/Kleinschreibung in der Regel nicht beachtet. Wenn Sie jedoch ein Benutzerkonto erstellen, das gelöscht oder in einer anderen Arbeitsgruppe erstellt wurde, muss die Groß-/Kleinschreibung beim Benutzernamen genau mit der Schreibweise des ursprünglichen Namens übereinstimmen. Bei Kennwörtern wird die Groß-/Kleinschreibung beachtet.

In der Regel erstellen Sie mit der **CreateWorkspace**-Methode ein **Workspace**-Objekt mit einem bestimmten Benutzernamen und Kennwort. Aus Gründen der Abwärtskompatibilität mit früheren Versionen und zur Arbeitserleichterung, wenn Sie keine sichere Datenbank implementieren, erstellt das Microsoft Access-Datenbankmodul automatisch bei Bedarf ein **Workspace**-Standardobjekt, falls noch keines geöffnet ist. In diesem Fall definieren die Werte der Eigenschaften **DefaultUser** und **DefaultPassword** den Benutzer und das Kennwort für das **Workspace**-Standardobjekt.

Damit diese Eigenschaft wirksam wird, müssen Sie sie festlegen, bevor Sie eine der DAO-Methoden aufrufen.

