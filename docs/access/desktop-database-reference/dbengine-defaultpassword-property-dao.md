---
title: DBEngine.DefaultPassword-Eigenschaft (DAO)
TOCTitle: DefaultPassword Property
ms:assetid: 189e34f3-d573-c75f-8be2-d98c50df8a52
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845616(v=office.15)
ms:contentKeyID: 48543478
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 72e73d29129c749d5479e2c7b17827f13adb4847
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28704735"
---
# <a name="dbenginedefaultpassword-property-dao"></a><span data-ttu-id="fde3b-102">DBEngine.DefaultPassword-Eigenschaft (DAO)</span><span class="sxs-lookup"><span data-stu-id="fde3b-102">DBEngine.DefaultPassword property (DAO)</span></span>


<span data-ttu-id="fde3b-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="fde3b-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="fde3b-p101">Legt das Kennwort fest, mit dem das Standardobjekt **Workspace** bei seiner Initialisierung erstellt wird. String-Wert mit Lese-/Schreibzugriff. **String**</span><span class="sxs-lookup"><span data-stu-id="fde3b-p101">Sets the password used to create the default **Workspace** when it is initialized. Read/write **String**.</span></span>

## <a name="syntax"></a><span data-ttu-id="fde3b-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="fde3b-106">Syntax</span></span>

<span data-ttu-id="fde3b-107">*Ausdruck* . DefaultPassword</span><span class="sxs-lookup"><span data-stu-id="fde3b-107">*expression* .DefaultPassword</span></span>

<span data-ttu-id="fde3b-108">*Ausdruck* Eine Variable, die ein **DBEngine** -Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="fde3b-108">*expression* A variable that represents a **DBEngine** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="fde3b-109">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="fde3b-109">Remarks</span></span>

<span data-ttu-id="fde3b-p102">Die Einstellung der DefaultPassword-Eigenschaft ist ein Wert vom Datentyp String, der bis zu 20 Zeichen lang sein kann. Mit Ausnahme von ASCII 0 kann er jedes Zeichen enthalten.</span><span class="sxs-lookup"><span data-stu-id="fde3b-p102">The setting for **DefaultPassword** is a String data type that can be up to 20 characters long. It can contain any character except ASCII 0.</span></span>


> [!NOTE]
> <span data-ttu-id="fde3b-p103">[!HINWEIS] Verwenden Sie sichere Kennwörter aus Groß- und Kleinbuchstaben, Zahlen und Symbolen. Unsichere Kennwörter enthalten keine Kombination dieser Elemente. Sicheres Kennwort: Y6dh!et5. Unsicheres Kennwort: Haus27. Verwenden Sie ein sicheres Kennwort, das Sie sich gut merken können, damit Sie es nicht aufschreiben müssen.</span><span class="sxs-lookup"><span data-stu-id="fde3b-p103">Use strong passwords that combine upper- and lowercase letters, numbers, and symbols. Weak passwords don't mix these elements. Strong password: Y6dh!et5. Weak password: House27. Use a strong password that you can remember so that you don't have to write it down.</span></span>

<span data-ttu-id="fde3b-117">Die **DefaultUser**-Eigenschaft ist standardmäßig auf "admin" und die **DefaultPassword**-Eigenschaft auf eine leere Zeichenfolge ("") festgelegt.</span><span class="sxs-lookup"><span data-stu-id="fde3b-117">By default, the **DefaultUser** property is set to "admin" and the **DefaultPassword** property is set to a zero-length string ("").</span></span>

<span data-ttu-id="fde3b-p104">In der Regel erstellen Sie mit der **CreateWorkspace**-Methode ein **Workspace**-Objekt mit einem bestimmten Benutzernamen und Kennwort. Aus Gründen der Abwärtskompatibilität mit früheren Versionen und zur Arbeitserleichterung, wenn Sie keine sichere Datenbank implementieren, erstellt das Microsoft Access-Datenbankmodul automatisch bei Bedarf ein **Workspace**-Standardobjekt, falls noch keines geöffnet ist. In diesem Fall definieren die Werte der Eigenschaften **DefaultUser** und **DefaultPassword** den Benutzer und das Kennwort für das **Workspace**-Standardobjekt.</span><span class="sxs-lookup"><span data-stu-id="fde3b-p104">Typically, you use the **CreateWorkspace** method to create a **Workspace** object with a given user name and password. However, for backward compatibility with earlier versions and for convenience when you don't implement a secured database, the Microsoft Access database engine automatically creates a default **Workspace** object when needed if one isn't already open. In this case, the **DefaultUser** and **DefaultPassword** property values define the user and password for the default **Workspace** object.</span></span>

<span data-ttu-id="fde3b-121">Damit diese Eigenschaft wirksam wird, müssen Sie sie festlegen, bevor Sie eine der DAO-Methoden aufrufen.</span><span class="sxs-lookup"><span data-stu-id="fde3b-121">For this property to take effect, you should set it before calling any DAO methods.</span></span>

