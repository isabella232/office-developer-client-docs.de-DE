---
title: Workspace.CreateDatabase-Methode (DAO)
TOCTitle: CreateDatabase Method
ms:assetid: c0ad986e-3b4d-f781-f782-5aa3cdccea7d
ms:mtpsurl: https://msdn.microsoft.com/library/Ff822832(v=office.15)
ms:contentKeyID: 48547514
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 5774eb4c9965cad7679d37754fd9a1f431ddaa48
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/02/2018
ms.locfileid: "25923413"
---
# <a name="workspacecreatedatabase-method-dao"></a><span data-ttu-id="a3e3f-102">Workspace.CreateDatabase-Methode (DAO)</span><span class="sxs-lookup"><span data-stu-id="a3e3f-102">Workspace.CreateDatabase method (DAO)</span></span>


<span data-ttu-id="a3e3f-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="a3e3f-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="a3e3f-104">Erstellt ein neues **[Database](database-object-dao.md)** -Objekt, speichert die Datenbank auf einem Datenträger und gibt ein geöffnetes **Database**-Objekt zurück (gilt nur für Microsoft Access-Arbeitsbereiche).</span><span class="sxs-lookup"><span data-stu-id="a3e3f-104">Creates a new **[Database](database-object-dao.md)** object, saves the database to disk, and returns an opened **Database** object (Microsoft Access workspaces only).</span></span>

## <a name="syntax"></a><span data-ttu-id="a3e3f-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="a3e3f-105">Syntax</span></span>

<span data-ttu-id="a3e3f-106">*Ausdruck* . CreateDatabase (***Name***, ***eine Verbindung herstellen***, ***Option***)</span><span class="sxs-lookup"><span data-stu-id="a3e3f-106">*expression* .CreateDatabase(***Name***, ***Connect***, ***Option***)</span></span>

<span data-ttu-id="a3e3f-107">*Ausdruck* Eine Variable, die ein **Workspace** -Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="a3e3f-107">*expression* A variable that represents a **Workspace** object.</span></span>

### <a name="parameters"></a><span data-ttu-id="a3e3f-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="a3e3f-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="a3e3f-109">Name</span><span class="sxs-lookup"><span data-stu-id="a3e3f-109">Name</span></span></p></th>
<th><p><span data-ttu-id="a3e3f-110">Erforderlich/Optional</span><span class="sxs-lookup"><span data-stu-id="a3e3f-110">Required/Optional</span></span></p></th>
<th><p><span data-ttu-id="a3e3f-111">Datentyp</span><span class="sxs-lookup"><span data-stu-id="a3e3f-111">Data Type</span></span></p></th>
<th><p><span data-ttu-id="a3e3f-112">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a3e3f-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a3e3f-113">Name</span><span class="sxs-lookup"><span data-stu-id="a3e3f-113">Name</span></span></p></td>
<td><p><span data-ttu-id="a3e3f-114">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="a3e3f-114">Required</span></span></p></td>
<td><p><span data-ttu-id="a3e3f-115"><strong>String</strong></span><span class="sxs-lookup"><span data-stu-id="a3e3f-115"><strong>String</strong></span></span></p></td>
<td><p><span data-ttu-id="a3e3f-116">Eine Zeichenfolge bis zu 255 Zeichen lang sein darf, die den Namen der Datenbankdatei ist, den Sie erstellen.</span><span class="sxs-lookup"><span data-stu-id="a3e3f-116">A String up to 255 characters long that is the name of the database file that you're creating.</span></span> <span data-ttu-id="a3e3f-117">Der vollständige Pfad und der Dateiname kann sein.</span><span class="sxs-lookup"><span data-stu-id="a3e3f-117">It can be the full path and file name.</span></span> <span data-ttu-id="a3e3f-118">Wenn Ihr Netzwerk unterstützt, Sie können auch angeben einen Netzwerkpfad wie &quot; \\server1\share1\dir1\db1&quot;.</span><span class="sxs-lookup"><span data-stu-id="a3e3f-118">If your network supports it, you can also specify a network path, such as &quot;\\server1\share1\dir1\db1&quot;.</span></span> <span data-ttu-id="a3e3f-119">Sie können mit dieser Methode nur Microsoft Access-Datenbankdateien erstellen.</span><span class="sxs-lookup"><span data-stu-id="a3e3f-119">You can only create Microsoft Access database files with this method.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a3e3f-120">Verbinden</span><span class="sxs-lookup"><span data-stu-id="a3e3f-120">Connect</span></span></p></td>
<td><p><span data-ttu-id="a3e3f-121">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="a3e3f-121">Required</span></span></p></td>
<td><p><span data-ttu-id="a3e3f-122"><strong>String</strong></span><span class="sxs-lookup"><span data-stu-id="a3e3f-122"><strong>String</strong></span></span></p></td>
<td><ul>
<li><p><span data-ttu-id="a3e3f-p102">Ein Zeichenfolgenausdruck, der eine Sortierreihenfolge zum Erstellen der Datenbank angibt, wie unter Einstellungen festgelegt. Wenn Sie dieses Argument nicht angeben, tritt ein Fehler auf.</span><span class="sxs-lookup"><span data-stu-id="a3e3f-p102">A string expression that specifies a collating order for creating the database, as specified in Settings. You must supply this argument or an error occurs.</span></span></p></li>
<li><p><span data-ttu-id="a3e3f-125">Sie können auch ein Kennwort für das neue <strong>Database</strong> -Objekt erstellen, indem Sie die Kennwortzeichenfolge (beginnend mit &quot;; Pwd =&quot;) mit einer Konstante im Argument <em>Locale</em> verknüpfen, wie folgt:</span><span class="sxs-lookup"><span data-stu-id="a3e3f-125">You can also create a password for the new <strong>Database</strong> object by concatenating the password string (starting with &quot;;pwd=&quot;) with a constant in the <em>locale</em> argument, like this:</span></span></p></li>
<li><p><span data-ttu-id="a3e3f-126">DbLangSpanish &amp; &quot;; Pwd = NewPassword&quot;</span><span class="sxs-lookup"><span data-stu-id="a3e3f-126">dbLangSpanish &amp; &quot;;pwd=NewPassword&quot;</span></span></p></li>
<li><p><span data-ttu-id="a3e3f-127">Wenn Sie das standardmäßige <em>locale</em> verwenden möchten, aber ein Kennwort angeben, geben Sie für das Argument <em>locale</em> einfach eine Kennwortzeichenfolge an:</span><span class="sxs-lookup"><span data-stu-id="a3e3f-127">If you want to use the default <em>locale</em>, but specify a password, simply enter a password string for the <em>locale</em> argument:</span></span></p></li>
<li><p><span data-ttu-id="a3e3f-128">&quot;; Pwd = NewPassword&quot;</span><span class="sxs-lookup"><span data-stu-id="a3e3f-128">&quot;;pwd=NewPassword&quot;</span></span></p></li>
<li><p><span data-ttu-id="a3e3f-p103">[!HINWEIS] Verwenden Sie sichere Kennwörter aus Groß- und Kleinbuchstaben, Zahlen und Symbolen. Unsichere Kennwörter enthalten keine Kombination dieser Elemente. Sicheres Kennwort: Y6dh!et5. Unsicheres Kennwort: Haus27. Verwenden Sie ein sicheres Kennwort, das Sie sich gut merken können, damit Sie es nicht aufschreiben müssen.</span><span class="sxs-lookup"><span data-stu-id="a3e3f-p103">Use strong passwords that combine upper- and lowercase letters, numbers, and symbols. Weak passwords don't mix these elements. Strong password: Y6dh!et5. Weak password: House27. Use a strong password that you can remember so that you don't have to write it down.</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a3e3f-134">Option</span><span class="sxs-lookup"><span data-stu-id="a3e3f-134">Option</span></span></p></td>
<td><p><span data-ttu-id="a3e3f-135">Optional</span><span class="sxs-lookup"><span data-stu-id="a3e3f-135">Optional</span></span></p></td>
<td><p><span data-ttu-id="a3e3f-136"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="a3e3f-136"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="a3e3f-p104">Eine Konstante oder eine Kombination aus Konstanten, die eine oder mehrere Optionen angibt, wie unter Einstellungen festgelegt. Sie können Optionen kombinieren, indem Sie die Summe der entsprechenden Konstanten bilden.</span><span class="sxs-lookup"><span data-stu-id="a3e3f-p104">A constant or combination of constants that indicates one or more options, as specified in Settings. You can combine options by summing the corresponding constants.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="a3e3f-139">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a3e3f-139">Remarks</span></span>

<span data-ttu-id="a3e3f-140">Sie können eine der folgenden Konstanten für das Argument locale verwenden, um die [CollatingOrder](database-collatingorder-property-dao.md)-Eigenschaft von Text für Zeichenfolgenvergleiche anzugeben.</span><span class="sxs-lookup"><span data-stu-id="a3e3f-140">You can use one of the following constants for the locale argument to specify the [CollatingOrder](database-collatingorder-property-dao.md) property of text for string comparisons.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="a3e3f-141">Konstante</span><span class="sxs-lookup"><span data-stu-id="a3e3f-141">Constant</span></span></p></th>
<th><p><span data-ttu-id="a3e3f-142">Sortierreihenfolge</span><span class="sxs-lookup"><span data-stu-id="a3e3f-142">Collating order</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a3e3f-143"><strong>dbLangGeneral</strong></span><span class="sxs-lookup"><span data-stu-id="a3e3f-143"><strong>dbLangGeneral</strong></span></span></p></td>
<td><p><span data-ttu-id="a3e3f-144">Englisch, Deutsch, Französisch, Portugiesisch, Italienisch und modernes Spanisch</span><span class="sxs-lookup"><span data-stu-id="a3e3f-144">English, German, French, Portuguese, Italian, and Modern Spanish</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a3e3f-145"><strong>dbLangArabic</strong></span><span class="sxs-lookup"><span data-stu-id="a3e3f-145"><strong>dbLangArabic</strong></span></span></p></td>
<td><p><span data-ttu-id="a3e3f-146">Arabisch</span><span class="sxs-lookup"><span data-stu-id="a3e3f-146">Arabic</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a3e3f-147"><strong>dbLangChineseSimplified</strong></span><span class="sxs-lookup"><span data-stu-id="a3e3f-147"><strong>dbLangChineseSimplified</strong></span></span></p></td>
<td><p><span data-ttu-id="a3e3f-148">Chinesisch (Vereinfacht)</span><span class="sxs-lookup"><span data-stu-id="a3e3f-148">Simplified Chinese</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a3e3f-149"><strong>dbLangChineseTraditional</strong></span><span class="sxs-lookup"><span data-stu-id="a3e3f-149"><strong>dbLangChineseTraditional</strong></span></span></p></td>
<td><p><span data-ttu-id="a3e3f-150">Chinesisch (Traditionell)</span><span class="sxs-lookup"><span data-stu-id="a3e3f-150">Traditional Chinese</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a3e3f-151"><strong>dbLangCyrillic</strong></span><span class="sxs-lookup"><span data-stu-id="a3e3f-151"><strong>dbLangCyrillic</strong></span></span></p></td>
<td><p><span data-ttu-id="a3e3f-152">Russisch</span><span class="sxs-lookup"><span data-stu-id="a3e3f-152">Russian</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a3e3f-153"><strong>dbLangCzech</strong></span><span class="sxs-lookup"><span data-stu-id="a3e3f-153"><strong>dbLangCzech</strong></span></span></p></td>
<td><p><span data-ttu-id="a3e3f-154">Tschechisch</span><span class="sxs-lookup"><span data-stu-id="a3e3f-154">Czech</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a3e3f-155"><strong>dbLangDutch</strong></span><span class="sxs-lookup"><span data-stu-id="a3e3f-155"><strong>dbLangDutch</strong></span></span></p></td>
<td><p><span data-ttu-id="a3e3f-156">Niederländisch</span><span class="sxs-lookup"><span data-stu-id="a3e3f-156">Dutch</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a3e3f-157"><strong>dbLangGreek</strong></span><span class="sxs-lookup"><span data-stu-id="a3e3f-157"><strong>dbLangGreek</strong></span></span></p></td>
<td><p><span data-ttu-id="a3e3f-158">Griechisch</span><span class="sxs-lookup"><span data-stu-id="a3e3f-158">Greek</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a3e3f-159"><strong>dbLangHebrew</strong></span><span class="sxs-lookup"><span data-stu-id="a3e3f-159"><strong>dbLangHebrew</strong></span></span></p></td>
<td><p><span data-ttu-id="a3e3f-160">Hebräisch</span><span class="sxs-lookup"><span data-stu-id="a3e3f-160">Hebrew</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a3e3f-161"><strong>dbLangHungarian</strong></span><span class="sxs-lookup"><span data-stu-id="a3e3f-161"><strong>dbLangHungarian</strong></span></span></p></td>
<td><p><span data-ttu-id="a3e3f-162">Ungarisch</span><span class="sxs-lookup"><span data-stu-id="a3e3f-162">Hungarian</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a3e3f-163"><strong>dbLangIcelandic</strong></span><span class="sxs-lookup"><span data-stu-id="a3e3f-163"><strong>dbLangIcelandic</strong></span></span></p></td>
<td><p><span data-ttu-id="a3e3f-164">Isländisch</span><span class="sxs-lookup"><span data-stu-id="a3e3f-164">Icelandic</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a3e3f-165"><strong>dbLangJapanese</strong></span><span class="sxs-lookup"><span data-stu-id="a3e3f-165"><strong>dbLangJapanese</strong></span></span></p></td>
<td><p><span data-ttu-id="a3e3f-166">Japanisch</span><span class="sxs-lookup"><span data-stu-id="a3e3f-166">Japanese</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a3e3f-167"><strong>dbLangKorean</strong></span><span class="sxs-lookup"><span data-stu-id="a3e3f-167"><strong>dbLangKorean</strong></span></span></p></td>
<td><p><span data-ttu-id="a3e3f-168">Koreanisch</span><span class="sxs-lookup"><span data-stu-id="a3e3f-168">Korean</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a3e3f-169"><strong>dbLangNordic</strong></span><span class="sxs-lookup"><span data-stu-id="a3e3f-169"><strong>dbLangNordic</strong></span></span></p></td>
<td><p><span data-ttu-id="a3e3f-170">Nordeuropäische Sprachen (nur Version 1.0 des Microsoft Jet-Datenbankmoduls)</span><span class="sxs-lookup"><span data-stu-id="a3e3f-170">Nordic languages (Microsoft Jet database engine version 1.0 only)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a3e3f-171"><strong>dbLangNorwDan</strong></span><span class="sxs-lookup"><span data-stu-id="a3e3f-171"><strong>dbLangNorwDan</strong></span></span></p></td>
<td><p><span data-ttu-id="a3e3f-172">Norwegisch und Dänisch</span><span class="sxs-lookup"><span data-stu-id="a3e3f-172">Norwegian and Danish</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a3e3f-173"><strong>dbLangPolish</strong></span><span class="sxs-lookup"><span data-stu-id="a3e3f-173"><strong>dbLangPolish</strong></span></span></p></td>
<td><p><span data-ttu-id="a3e3f-174">Polnisch</span><span class="sxs-lookup"><span data-stu-id="a3e3f-174">Polish</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a3e3f-175"><strong>dbLangSlovenian</strong></span><span class="sxs-lookup"><span data-stu-id="a3e3f-175"><strong>dbLangSlovenian</strong></span></span></p></td>
<td><p><span data-ttu-id="a3e3f-176">Slowenisch</span><span class="sxs-lookup"><span data-stu-id="a3e3f-176">Slovenian</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a3e3f-177"><strong>dbLangSpanish</strong></span><span class="sxs-lookup"><span data-stu-id="a3e3f-177"><strong>dbLangSpanish</strong></span></span></p></td>
<td><p><span data-ttu-id="a3e3f-178">Spanisch (Traditionell)</span><span class="sxs-lookup"><span data-stu-id="a3e3f-178">Traditional Spanish</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a3e3f-179"><strong>dbLangSwedFin</strong></span><span class="sxs-lookup"><span data-stu-id="a3e3f-179"><strong>dbLangSwedFin</strong></span></span></p></td>
<td><p><span data-ttu-id="a3e3f-180">Schwedisch und Finnisch</span><span class="sxs-lookup"><span data-stu-id="a3e3f-180">Swedish and Finnish</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a3e3f-181"><strong>dbLangThai</strong></span><span class="sxs-lookup"><span data-stu-id="a3e3f-181"><strong>dbLangThai</strong></span></span></p></td>
<td><p><span data-ttu-id="a3e3f-182">Thailändisch</span><span class="sxs-lookup"><span data-stu-id="a3e3f-182">Thai</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a3e3f-183"><strong>dbLangTurkish</strong></span><span class="sxs-lookup"><span data-stu-id="a3e3f-183"><strong>dbLangTurkish</strong></span></span></p></td>
<td><p><span data-ttu-id="a3e3f-184">Türkisch</span><span class="sxs-lookup"><span data-stu-id="a3e3f-184">Turkish</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="a3e3f-185">Sie können eine oder mehrere der folgenden Konstanten im Argument options verwenden, um anzugeben, welche Version das Datenformat haben soll und ob die Datenbank verschlüsselt werden soll.</span><span class="sxs-lookup"><span data-stu-id="a3e3f-185">You can use one or more of the following constants in the options argument to specify which version the data format should have and whether or not to encrypt the database.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="a3e3f-186">Konstante</span><span class="sxs-lookup"><span data-stu-id="a3e3f-186">Constant</span></span></p></th>
<th><p><span data-ttu-id="a3e3f-187">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a3e3f-187">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a3e3f-188"><strong>dbEncrypt</strong></span><span class="sxs-lookup"><span data-stu-id="a3e3f-188"><strong>dbEncrypt</strong></span></span></p></td>
<td><p><span data-ttu-id="a3e3f-189">Erstellt eine verschlüsselte Datenbank.</span><span class="sxs-lookup"><span data-stu-id="a3e3f-189">Creates an encrypted database.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a3e3f-190"><strong>dbVersion10</strong></span><span class="sxs-lookup"><span data-stu-id="a3e3f-190"><strong>dbVersion10</strong></span></span></p></td>
<td><p><span data-ttu-id="a3e3f-191">Erstellt eine Datenbank, die das Dateiformat der Version 1.0 des Microsoft Jet-Datenbankmoduls verwendet.</span><span class="sxs-lookup"><span data-stu-id="a3e3f-191">Creates a database that uses the Microsoft Jet database engine version 1.0 file format.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a3e3f-192"><strong>dbVersion11</strong></span><span class="sxs-lookup"><span data-stu-id="a3e3f-192"><strong>dbVersion11</strong></span></span></p></td>
<td><p><span data-ttu-id="a3e3f-193">Erstellt eine Datenbank, die das Dateiformat der Version 1.1 des Microsoft Jet-Datenbankmoduls verwendet.</span><span class="sxs-lookup"><span data-stu-id="a3e3f-193">Creates a database that uses the Microsoft Jet database engine version 1.1 file format.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a3e3f-194"><strong>dbVersion20</strong></span><span class="sxs-lookup"><span data-stu-id="a3e3f-194"><strong>dbVersion20</strong></span></span></p></td>
<td><p><span data-ttu-id="a3e3f-195">Erstellt eine Datenbank, die das Dateiformat der Version 2.0 des Microsoft Jet-Datenbankmoduls verwendet.</span><span class="sxs-lookup"><span data-stu-id="a3e3f-195">Creates a database that uses the Microsoft Jet database engine version 2.0 file format.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a3e3f-196"><strong>dbVersion30</strong></span><span class="sxs-lookup"><span data-stu-id="a3e3f-196"><strong>dbVersion30</strong></span></span></p></td>
<td><p><span data-ttu-id="a3e3f-197">Erstellt eine Datenbank, die das Dateiformat der Version 3.0 des Microsoft Jet-Datenbankmoduls verwendet (kompatibel mit Version 3.5).</span><span class="sxs-lookup"><span data-stu-id="a3e3f-197">Creates a database that uses the Microsoft Jet database engine version 3.0 file format (compatible with version 3.5).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a3e3f-198"><strong>dbVersion40</strong></span><span class="sxs-lookup"><span data-stu-id="a3e3f-198"><strong>dbVersion40</strong></span></span></p></td>
<td><p><span data-ttu-id="a3e3f-199">Erstellt eine Datenbank, die das Dateiformat der Version 4.0 des Microsoft Jet-Datenbankmoduls verwendet.</span><span class="sxs-lookup"><span data-stu-id="a3e3f-199">Creates a database that uses the Microsoft Jet database engine version 4.0 file format.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a3e3f-200"><strong>dbVersion120</strong></span><span class="sxs-lookup"><span data-stu-id="a3e3f-200"><strong>dbVersion120</strong></span></span></p></td>
<td><p><span data-ttu-id="a3e3f-201">Erstellt eine Datenbank, die das Dateiformat der Version 12.0 des Microsoft Access-Datenbankmoduls verwendet.</span><span class="sxs-lookup"><span data-stu-id="a3e3f-201">Creates a database that uses the Microsoft Access database engine version 12.0 file format.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="a3e3f-202">Wenn Sie die Verschlüsselungskonstante weglassen, erstellt **CreateDatabase** eine nicht verschlüsselte Datenbank.</span><span class="sxs-lookup"><span data-stu-id="a3e3f-202">If you omit the encryption constant, **CreateDatabase** creates an un-encrypted database.</span></span>

<span data-ttu-id="a3e3f-p105">Verwenden Sie die **CreateDatabase**-Methode zum Erstellen und Öffnen einer neuen, leeren Datenbank, und geben Sie das **Database**-Objekt zurück. Mithilfe zusätzlicher DAO-Objekte müssen Sie dessen Struktur und Inhalt vollständig angeben. Wenn Sie eine vorhandene Datenbank teilweise oder vollständig kopieren möchten, können Sie unter Verwendung der **[CompactDatabase](dbengine-compactdatabase-method-dao.md)** -Methode eine Kopie erstellen und diese anpassen.</span><span class="sxs-lookup"><span data-stu-id="a3e3f-p105">Use the **CreateDatabase** method to create and open a new, empty database, and return the **Database** object. You must complete its structure and content by using additional DAO objects. If you want to make a partial or complete copy of an existing database, you can use the **[CompactDatabase](dbengine-compactdatabase-method-dao.md)** method to make a copy that you can customize.</span></span>

## <a name="example"></a><span data-ttu-id="a3e3f-206">Beispiel</span><span class="sxs-lookup"><span data-stu-id="a3e3f-206">Example</span></span>

<span data-ttu-id="a3e3f-207">In diesem Beispiel wird mithilfe von **CreateDatabase** ein neues, verschlüsseltes **Database**-Objekt erstellt.</span><span class="sxs-lookup"><span data-stu-id="a3e3f-207">This example uses **CreateDatabase** to create a new, encrypted **Database** object.</span></span>

```vb
    Sub CreateDatabaseX() 
     
       Dim wrkDefault As Workspace 
       Dim dbsNew As DATABASE 
       Dim prpLoop As Property 
     
       ' Get default Workspace. 
       Set wrkDefault = DBEngine.Workspaces(0) 
     
       ' Make sure there isn't already a file with the name of  
       ' the new database. 
       If Dir("NewDB.mdb") <> "" Then Kill "NewDB.mdb" 
     
       ' Create a new encrypted database with the specified  
       ' collating order. 
       Set dbsNew = wrkDefault.CreateDatabase("NewDB.mdb", _ 
          dbLangGeneral, dbEncrypt) 
     
       With dbsNew 
          Debug.Print "Properties of " & .Name 
          ' Enumerate the Properties collection of the new  
          ' Database object. 
          For Each prpLoop In .Properties 
             If prpLoop <> "" Then Debug.Print "  " & _ 
                prpLoop.Name & " = " & prpLoop 
          Next prpLoop 
       End With 
     
       dbsNew.Close 
     
    End Sub
```
