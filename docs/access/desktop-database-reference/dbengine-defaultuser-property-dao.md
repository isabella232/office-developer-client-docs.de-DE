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
# <a name="dbenginedefaultuser-property-dao"></a><span data-ttu-id="ebcaf-102">DbEngine. DefaultUser-Eigenschaft (DAO)</span><span class="sxs-lookup"><span data-stu-id="ebcaf-102">DBEngine.DefaultUser property (DAO)</span></span>


<span data-ttu-id="ebcaf-103">**Gilt für**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="ebcaf-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="ebcaf-104">Legt den Benutzernamen fest, mit dem das Standardobjekt **Workspace** bei seiner Initialisierung erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="ebcaf-104">Sets the user name used to create the default **Workspace** when it is initialized.</span></span> <span data-ttu-id="ebcaf-105">**String**-Wert mit Lese-/Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="ebcaf-105">Read/write **String**.</span></span>

## <a name="syntax"></a><span data-ttu-id="ebcaf-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="ebcaf-106">Syntax</span></span>

<span data-ttu-id="ebcaf-107">*Ausdruck* . DefaultUser</span><span class="sxs-lookup"><span data-stu-id="ebcaf-107">*expression* .DefaultUser</span></span>

<span data-ttu-id="ebcaf-108">*Ausdruck* Ein Ausdruck, der ein **DBEngine** -Objekt zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="ebcaf-108">*expression* An expression that returns a **DBEngine** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="ebcaf-109">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ebcaf-109">Remarks</span></span>

<span data-ttu-id="ebcaf-110">The setting for **DefaultUser** is a String data type.</span><span class="sxs-lookup"><span data-stu-id="ebcaf-110">The setting for **DefaultUser** is a String data type.</span></span> <span data-ttu-id="ebcaf-111">Es kann 1 bis 20 Zeichen lang in Microsoft Access-Arbeitsbereichen, und es kann alphabetische Zeichen, Akzentzeichen, Zahlen, Leerzeichen und Symbole enthalten, mit Ausnahme von: "(Anführungszeichen),/( \\ Schrägstrich), \[ \] (Backslash), (Klammern) ,: (Doppelpunkt), | (Pipe), \< (kleiner-als-Zeichen) \> , (größer-als-Zeichen), + (Pluszeichen), = (Gleichheitszeichen),; (Semikolon),, (Komma),?</span><span class="sxs-lookup"><span data-stu-id="ebcaf-111">It can be 1–20 characters long in Microsoft Access workspaces and it can include alphabetic characters, accented characters, numbers, spaces, and symbols except for: " (quotation marks), / (forward slash), \\ (backslash), \[ \] (brackets), : (colon), | (pipe), \< (less-than sign), \> (greater-than sign), + (plus sign), = (equal sign), ; (semicolon), , ( comma), ?</span></span> <span data-ttu-id="ebcaf-112">(Fragezeichen), \* (Asterisk), führende Leerzeichen und Steuerelemente (ASCII 00 bis ASCII 31).</span><span class="sxs-lookup"><span data-stu-id="ebcaf-112">(question mark), \* (asterisk), leading spaces, and control characters (ASCII 00 to ASCII 31).</span></span>


> [!NOTE]
> <span data-ttu-id="ebcaf-p103">[!HINWEIS] Verwenden Sie sichere Kennwörter aus Groß- und Kleinbuchstaben, Zahlen und Symbolen. Unsichere Kennwörter enthalten keine Kombination dieser Elemente. Sicheres Kennwort: Y6dh!et5. Unsicheres Kennwort: Haus27. Verwenden Sie ein sicheres Kennwort, das Sie sich gut merken können, damit Sie es nicht aufschreiben müssen.</span><span class="sxs-lookup"><span data-stu-id="ebcaf-p103">Use strong passwords that combine upper- and lowercase letters, numbers, and symbols. Weak passwords don't mix these elements. Strong password: Y6dh!et5. Weak password: House27. Use a strong password that you can remember so that you don't have to write it down.</span></span>

<span data-ttu-id="ebcaf-118">Die **DefaultUser**-Eigenschaft ist standardmäßig auf "admin" und die **DefaultPassword**-Eigenschaft auf eine leere Zeichenfolge ("") festgelegt.</span><span class="sxs-lookup"><span data-stu-id="ebcaf-118">By default, the **DefaultUser** property is set to "admin" and the **DefaultPassword** property is set to a zero-length string ("").</span></span>

<span data-ttu-id="ebcaf-p104">Bei Benutzernamen wird die Groß-/Kleinschreibung in der Regel nicht beachtet. Wenn Sie jedoch ein Benutzerkonto erstellen, das gelöscht oder in einer anderen Arbeitsgruppe erstellt wurde, muss die Groß-/Kleinschreibung beim Benutzernamen genau mit der Schreibweise des ursprünglichen Namens übereinstimmen. Bei Kennwörtern wird die Groß-/Kleinschreibung beachtet.</span><span class="sxs-lookup"><span data-stu-id="ebcaf-p104">User names aren't usually case-sensitive; however, if you're re-creating a user account that was deleted or created in a different workgroup, the user name must be an exact case-sensitive match of the original name. Passwords are case-sensitive.</span></span>

<span data-ttu-id="ebcaf-p105">In der Regel erstellen Sie mit der **CreateWorkspace**-Methode ein **Workspace**-Objekt mit einem bestimmten Benutzernamen und Kennwort. Aus Gründen der Abwärtskompatibilität mit früheren Versionen und zur Arbeitserleichterung, wenn Sie keine sichere Datenbank implementieren, erstellt das Microsoft Access-Datenbankmodul automatisch bei Bedarf ein **Workspace**-Standardobjekt, falls noch keines geöffnet ist. In diesem Fall definieren die Werte der Eigenschaften **DefaultUser** und **DefaultPassword** den Benutzer und das Kennwort für das **Workspace**-Standardobjekt.</span><span class="sxs-lookup"><span data-stu-id="ebcaf-p105">Typically, you use the **CreateWorkspace** method to create a **Workspace** object with a given user name and password. However, for backward compatibility with earlier versions and for convenience when you don't implement a secured database, the Microsoft Access database engine automatically creates a default **Workspace** object when needed if one isn't already open. In this case, the **DefaultUser** and **DefaultPassword** property values define the user and password for the default **Workspace** object.</span></span>

<span data-ttu-id="ebcaf-124">Damit diese Eigenschaft wirksam wird, müssen Sie sie festlegen, bevor Sie eine der DAO-Methoden aufrufen.</span><span class="sxs-lookup"><span data-stu-id="ebcaf-124">For this property to take effect, you should set it before calling any DAO methods.</span></span>

