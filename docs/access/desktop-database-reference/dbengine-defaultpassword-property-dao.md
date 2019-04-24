---
title: DbEngine. DefaultPassword-Eigenschaft (DAO)
TOCTitle: DefaultPassword Property
ms:assetid: 189e34f3-d573-c75f-8be2-d98c50df8a52
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845616(v=office.15)
ms:contentKeyID: 48543478
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 72e73d29129c749d5479e2c7b17827f13adb4847
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32294358"
---
# <a name="dbenginedefaultpassword-property-dao"></a>DbEngine. DefaultPassword-Eigenschaft (DAO)


**Gilt für**: Access 2013, Office 2013

Legt das Kennwort fest, mit dem der Standard **Arbeitsbereich** erstellt wird, wenn es initialisiert wird. **String**-Wert mit Lese-/Schreibzugriff.

## <a name="syntax"></a>Syntax

*Ausdruck* . DefaultPassword

*Ausdruck* Eine Variable, die ein **DBEngine** -Objekt darstellt.

## <a name="remarks"></a>Bemerkungen

The setting for **DefaultPassword** is a String data type that can be up to 20 characters long. It can contain any character except ASCII 0.


> [!NOTE]
> [!HINWEIS] Verwenden Sie sichere Kennwörter aus Groß- und Kleinbuchstaben, Zahlen und Symbolen. Unsichere Kennwörter enthalten keine Kombination dieser Elemente. Sicheres Kennwort: Y6dh!et5. Unsicheres Kennwort: Haus27. Verwenden Sie ein sicheres Kennwort, das Sie sich gut merken können, damit Sie es nicht aufschreiben müssen.

Die **DefaultUser**-Eigenschaft ist standardmäßig auf "admin" und die **DefaultPassword**-Eigenschaft auf eine leere Zeichenfolge ("") festgelegt.

In der Regel erstellen Sie mit der **CreateWorkspace**-Methode ein **Workspace**-Objekt mit einem bestimmten Benutzernamen und Kennwort. Aus Gründen der Abwärtskompatibilität mit früheren Versionen und zur Arbeitserleichterung, wenn Sie keine sichere Datenbank implementieren, erstellt das Microsoft Access-Datenbankmodul automatisch bei Bedarf ein **Workspace**-Standardobjekt, falls noch keines geöffnet ist. In diesem Fall definieren die Werte der Eigenschaften **DefaultUser** und **DefaultPassword** den Benutzer und das Kennwort für das **Workspace**-Standardobjekt.

Damit diese Eigenschaft wirksam wird, müssen Sie sie festlegen, bevor Sie eine der DAO-Methoden aufrufen.

