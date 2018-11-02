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
ms.openlocfilehash: 48397c3654d11735d13dd9499e1a6784f330f4af
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/02/2018
ms.locfileid: "25927149"
---
# <a name="dbenginedefaultuser-property-dao"></a><span data-ttu-id="7c780-102">DBEngine.DefaultUser-Eigenschaft (DAO)</span><span class="sxs-lookup"><span data-stu-id="7c780-102">DBEngine.DefaultUser property (DAO)</span></span>


<span data-ttu-id="7c780-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="7c780-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="7c780-p101">Legt den Benutzernamen fest, mit dem das Standardobjekt **Workspace** bei seiner Initialisierung erstellt wird. **String**-Wert mit Lese-/Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="7c780-p101">Sets the user name used to create the default **Workspace** when it is initialized. Read/write **String**.</span></span>

## <a name="syntax"></a><span data-ttu-id="7c780-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="7c780-106">Syntax</span></span>

<span data-ttu-id="7c780-107">*Ausdruck* . DefaultUser</span><span class="sxs-lookup"><span data-stu-id="7c780-107">*expression* .DefaultUser</span></span>

<span data-ttu-id="7c780-108">*Ausdruck* Ein Ausdruck, der ein **DBEngine** -Objekt zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="7c780-108">*expression* An expression that returns a **DBEngine** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="7c780-109">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7c780-109">Remarks</span></span>

<span data-ttu-id="7c780-110">Die Einstellung für **DefaultUser** ist vom Datentyp String.</span><span class="sxs-lookup"><span data-stu-id="7c780-110">The setting for **DefaultUser** is a String data type.</span></span> <span data-ttu-id="7c780-111">1 bis 20 Zeichen lange in Microsoft Access-Arbeitsbereiche und es können enthalten alphabetische Zeichen, Akzentbuchstaben, Zahlen, Leerzeichen und Symbole mit Ausnahme von: "(Anführungszeichen) / (Schrägstrich), \\ (umgekehrter Schrägstrich), \[ \] (Klammern) ,: (Doppelpunkt), | (Pipe), \< (kleiner-als-Zeichen), \> (größer-als-Zeichen), + (Pluszeichen), = (Gleichheitszeichen), (Semikolon), (Komma)?</span><span class="sxs-lookup"><span data-stu-id="7c780-111">It can be 1–20 characters long in Microsoft Access workspaces and it can include alphabetic characters, accented characters, numbers, spaces, and symbols except for: " (quotation marks), / (forward slash), \\ (backslash), \[ \] (brackets), : (colon), | (pipe), \< (less-than sign), \> (greater-than sign), + (plus sign), = (equal sign), ; (semicolon), , ( comma), ?</span></span> <span data-ttu-id="7c780-112">(Fragezeichen) \* (Sternchen), führende Leerzeichen und Steuerzeichen (ASCII 00 bis ASCII 31).</span><span class="sxs-lookup"><span data-stu-id="7c780-112">(question mark), \* (asterisk), leading spaces, and control characters (ASCII 00 to ASCII 31).</span></span>


> [!NOTE]
> <span data-ttu-id="7c780-p103">[!HINWEIS] Verwenden Sie sichere Kennwörter aus Groß- und Kleinbuchstaben, Zahlen und Symbolen. Unsichere Kennwörter enthalten keine Kombination dieser Elemente. Sicheres Kennwort: Y6dh!et5. Unsicheres Kennwort: Haus27. Verwenden Sie ein sicheres Kennwort, das Sie sich gut merken können, damit Sie es nicht aufschreiben müssen.</span><span class="sxs-lookup"><span data-stu-id="7c780-p103">Use strong passwords that combine upper- and lowercase letters, numbers, and symbols. Weak passwords don't mix these elements. Strong password: Y6dh!et5. Weak password: House27. Use a strong password that you can remember so that you don't have to write it down.</span></span>

<span data-ttu-id="7c780-118">Die **DefaultUser**-Eigenschaft ist standardmäßig auf "admin" und die **DefaultPassword**-Eigenschaft auf eine leere Zeichenfolge ("") festgelegt.</span><span class="sxs-lookup"><span data-stu-id="7c780-118">By default, the **DefaultUser** property is set to "admin" and the **DefaultPassword** property is set to a zero-length string ("").</span></span>

<span data-ttu-id="7c780-p104">Bei Benutzernamen wird die Groß-/Kleinschreibung in der Regel nicht beachtet. Wenn Sie jedoch ein Benutzerkonto erstellen, das gelöscht oder in einer anderen Arbeitsgruppe erstellt wurde, muss die Groß-/Kleinschreibung beim Benutzernamen genau mit der Schreibweise des ursprünglichen Namens übereinstimmen. Bei Kennwörtern wird die Groß-/Kleinschreibung beachtet.</span><span class="sxs-lookup"><span data-stu-id="7c780-p104">User names aren't usually case-sensitive; however, if you're re-creating a user account that was deleted or created in a different workgroup, the user name must be an exact case-sensitive match of the original name. Passwords are case-sensitive.</span></span>

<span data-ttu-id="7c780-p105">In der Regel erstellen Sie mit der **CreateWorkspace**-Methode ein **Workspace**-Objekt mit einem bestimmten Benutzernamen und Kennwort. Aus Gründen der Abwärtskompatibilität mit früheren Versionen und zur Arbeitserleichterung, wenn Sie keine sichere Datenbank implementieren, erstellt das Microsoft Access-Datenbankmodul automatisch bei Bedarf ein **Workspace**-Standardobjekt, falls noch keines geöffnet ist. In diesem Fall definieren die Werte der Eigenschaften **DefaultUser** und **DefaultPassword** den Benutzer und das Kennwort für das **Workspace**-Standardobjekt.</span><span class="sxs-lookup"><span data-stu-id="7c780-p105">Typically, you use the **CreateWorkspace** method to create a **Workspace** object with a given user name and password. However, for backward compatibility with earlier versions and for convenience when you don't implement a secured database, the Microsoft Access database engine automatically creates a default **Workspace** object when needed if one isn't already open. In this case, the **DefaultUser** and **DefaultPassword** property values define the user and password for the default **Workspace** object.</span></span>

<span data-ttu-id="7c780-124">Damit diese Eigenschaft wirksam wird, müssen Sie sie festlegen, bevor Sie eine der DAO-Methoden aufrufen.</span><span class="sxs-lookup"><span data-stu-id="7c780-124">For this property to take effect, you should set it before calling any DAO methods.</span></span>

