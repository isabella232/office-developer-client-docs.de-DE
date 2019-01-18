---
title: Workspace.CreateDatabase-Methode (DAO)
TOCTitle: CreateDatabase Method
ms:assetid: c0ad986e-3b4d-f781-f782-5aa3cdccea7d
ms:mtpsurl: https://msdn.microsoft.com/library/Ff822832(v=office.15)
ms:contentKeyID: 48547514
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: e6d271676ef91d29dca78ba9ee4b6142e055b36d
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28702131"
---
# <a name="workspacecreatedatabase-method-dao"></a><span data-ttu-id="97b7c-102">Workspace.CreateDatabase-Methode (DAO)</span><span class="sxs-lookup"><span data-stu-id="97b7c-102">Workspace.CreateDatabase method (DAO)</span></span>

<span data-ttu-id="97b7c-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="97b7c-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="97b7c-104">Erstellt ein neues **[Database](database-object-dao.md)** -Objekt, speichert die Datenbank auf einem Datenträger und gibt ein geöffnetes **Database**-Objekt zurück (gilt nur für Microsoft Access-Arbeitsbereiche).</span><span class="sxs-lookup"><span data-stu-id="97b7c-104">Creates a new **[Database](database-object-dao.md)** object, saves the database to disk, and returns an opened **Database** object (Microsoft Access workspaces only).</span></span>

## <a name="syntax"></a><span data-ttu-id="97b7c-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="97b7c-105">Syntax</span></span>

<span data-ttu-id="97b7c-106">*Ausdruck* . CreateDatabase (***Name***, ***eine Verbindung herstellen***, ***Option***)</span><span class="sxs-lookup"><span data-stu-id="97b7c-106">*expression* .CreateDatabase(***Name***, ***Connect***, ***Option***)</span></span>

<span data-ttu-id="97b7c-107">*Ausdruck* Eine Variable, die ein **Workspace** -Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="97b7c-107">*expression* A variable that represents a **Workspace** object.</span></span>

## <a name="parameters"></a><span data-ttu-id="97b7c-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="97b7c-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="97b7c-109">Name</span><span class="sxs-lookup"><span data-stu-id="97b7c-109">Name</span></span></p></th>
<th><p><span data-ttu-id="97b7c-110">Erforderlich oder optional</span><span class="sxs-lookup"><span data-stu-id="97b7c-110">Required/optional</span></span></p></th>
<th><p><span data-ttu-id="97b7c-111">Datentyp</span><span class="sxs-lookup"><span data-stu-id="97b7c-111">Data type</span></span></p></th>
<th><p><span data-ttu-id="97b7c-112">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="97b7c-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="97b7c-113"><em>Name</em></span><span class="sxs-lookup"><span data-stu-id="97b7c-113"><em>Name</em></span></span></p></td>
<td><p><span data-ttu-id="97b7c-114">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="97b7c-114">Required</span></span></p></td>
<td><p><span data-ttu-id="97b7c-115"><strong>String</strong></span><span class="sxs-lookup"><span data-stu-id="97b7c-115"><strong>String</strong></span></span></p></td>
<td><p><span data-ttu-id="97b7c-116">Eine Zeichenfolge bis zu 255 Zeichen lang sein darf, die den Namen der Datenbankdatei ist, den Sie erstellen.</span><span class="sxs-lookup"><span data-stu-id="97b7c-116">A String up to 255 characters long that is the name of the database file that you're creating.</span></span> <span data-ttu-id="97b7c-117">Der vollständige Pfad und der Dateiname kann sein.</span><span class="sxs-lookup"><span data-stu-id="97b7c-117">It can be the full path and file name.</span></span> <span data-ttu-id="97b7c-118">Wenn Ihr Netzwerk unterstützt, Sie können auch angeben einen Netzwerkpfad wie &quot; \\server1\share1\dir1\db1&quot;.</span><span class="sxs-lookup"><span data-stu-id="97b7c-118">If your network supports it, you can also specify a network path, such as &quot;\\server1\share1\dir1\db1&quot;.</span></span> <span data-ttu-id="97b7c-119">Sie können mit dieser Methode nur Microsoft Access-Datenbankdateien erstellen.</span><span class="sxs-lookup"><span data-stu-id="97b7c-119">You can only create Microsoft Access database files with this method.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="97b7c-120"><em>Connect</em></span><span class="sxs-lookup"><span data-stu-id="97b7c-120"><em>Connect</em></span></span></p></td>
<td><p><span data-ttu-id="97b7c-121">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="97b7c-121">Required</span></span></p></td>
<td><p><span data-ttu-id="97b7c-122"><strong>String</strong></span><span class="sxs-lookup"><span data-stu-id="97b7c-122"><strong>String</strong></span></span></p></td>
<td><ul>
<li><p><span data-ttu-id="97b7c-p102">Ein Zeichenfolgenausdruck, der eine Sortierreihenfolge zum Erstellen der Datenbank angibt, wie unter Einstellungen festgelegt. Wenn Sie dieses Argument nicht angeben, tritt ein Fehler auf.</span><span class="sxs-lookup"><span data-stu-id="97b7c-p102">A string expression that specifies a collating order for creating the database, as specified in Settings. You must supply this argument or an error occurs.</span></span></p></li>
<li><p><span data-ttu-id="97b7c-125">Sie können auch ein Kennwort für das neue <strong>Database</strong> -Objekt erstellen, indem Sie die Kennwortzeichenfolge (beginnend mit &quot;; Pwd =&quot;) mit einer Konstante im Argument <em>Locale</em> verknüpfen, wie folgt:</span><span class="sxs-lookup"><span data-stu-id="97b7c-125">You can also create a password for the new <strong>Database</strong> object by concatenating the password string (starting with &quot;;pwd=&quot;) with a constant in the <em>locale</em> argument, like this:</span></span></p></li>
<li><p><span data-ttu-id="97b7c-126">DbLangSpanish &amp; &quot;; Pwd = NewPassword&quot;</span><span class="sxs-lookup"><span data-stu-id="97b7c-126">dbLangSpanish &amp; &quot;;pwd=NewPassword&quot;</span></span></p></li>
<li><p><span data-ttu-id="97b7c-127">Wenn Sie das standardmäßige <em>locale</em> verwenden möchten, aber ein Kennwort angeben, geben Sie für das Argument <em>locale</em> einfach eine Kennwortzeichenfolge an:</span><span class="sxs-lookup"><span data-stu-id="97b7c-127">If you want to use the default <em>locale</em>, but specify a password, simply enter a password string for the <em>locale</em> argument:</span></span></p></li>
<li><p><span data-ttu-id="97b7c-128">&quot;; Pwd = NewPassword&quot;</span><span class="sxs-lookup"><span data-stu-id="97b7c-128">&quot;;pwd=NewPassword&quot;</span></span></p></li>
<li><p><span data-ttu-id="97b7c-p103">[!HINWEIS] Verwenden Sie sichere Kennwörter aus Groß- und Kleinbuchstaben, Zahlen und Symbolen. Unsichere Kennwörter enthalten keine Kombination dieser Elemente. Sicheres Kennwort: Y6dh!et5. Unsicheres Kennwort: Haus27. Verwenden Sie ein sicheres Kennwort, das Sie sich gut merken können, damit Sie es nicht aufschreiben müssen.</span><span class="sxs-lookup"><span data-stu-id="97b7c-p103">Use strong passwords that combine upper- and lowercase letters, numbers, and symbols. Weak passwords don't mix these elements. Strong password: Y6dh!et5. Weak password: House27. Use a strong password that you can remember so that you don't have to write it down.</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="97b7c-134"><em>Option</em></span><span class="sxs-lookup"><span data-stu-id="97b7c-134"><em>Option</em></span></span></p></td>
<td><p><span data-ttu-id="97b7c-135">Optional</span><span class="sxs-lookup"><span data-stu-id="97b7c-135">Optional</span></span></p></td>
<td><p><span data-ttu-id="97b7c-136"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="97b7c-136"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="97b7c-p104">Eine Konstante oder eine Kombination aus Konstanten, die eine oder mehrere Optionen angibt, wie unter Einstellungen festgelegt. Sie können Optionen kombinieren, indem Sie die Summe der entsprechenden Konstanten bilden.</span><span class="sxs-lookup"><span data-stu-id="97b7c-p104">A constant or combination of constants that indicates one or more options, as specified in Settings. You can combine options by summing the corresponding constants.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="97b7c-139">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="97b7c-139">Remarks</span></span>

<span data-ttu-id="97b7c-140">Sie können eine der folgenden Konstanten für das Argument locale verwenden, um die [CollatingOrder](database-collatingorder-property-dao.md)-Eigenschaft von Text für Zeichenfolgenvergleiche anzugeben.</span><span class="sxs-lookup"><span data-stu-id="97b7c-140">You can use one of the following constants for the locale argument to specify the [CollatingOrder](database-collatingorder-property-dao.md) property of text for string comparisons.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="97b7c-141">Konstante</span><span class="sxs-lookup"><span data-stu-id="97b7c-141">Constant</span></span></p></th>
<th><p><span data-ttu-id="97b7c-142">Sortierreihenfolge</span><span class="sxs-lookup"><span data-stu-id="97b7c-142">Collating order</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="97b7c-143"><strong>dbLangGeneral</strong></span><span class="sxs-lookup"><span data-stu-id="97b7c-143"><strong>dbLangGeneral</strong></span></span></p></td>
<td><p><span data-ttu-id="97b7c-144">Englisch, Deutsch, Französisch, Portugiesisch, Italienisch und modernes Spanisch</span><span class="sxs-lookup"><span data-stu-id="97b7c-144">English, German, French, Portuguese, Italian, and Modern Spanish</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="97b7c-145"><strong>dbLangArabic</strong></span><span class="sxs-lookup"><span data-stu-id="97b7c-145"><strong>dbLangArabic</strong></span></span></p></td>
<td><p><span data-ttu-id="97b7c-146">Arabisch</span><span class="sxs-lookup"><span data-stu-id="97b7c-146">Arabic</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="97b7c-147"><strong>dbLangChineseSimplified</strong></span><span class="sxs-lookup"><span data-stu-id="97b7c-147"><strong>dbLangChineseSimplified</strong></span></span></p></td>
<td><p><span data-ttu-id="97b7c-148">Chinesisch (Vereinfacht)</span><span class="sxs-lookup"><span data-stu-id="97b7c-148">Simplified Chinese</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="97b7c-149"><strong>dbLangChineseTraditional</strong></span><span class="sxs-lookup"><span data-stu-id="97b7c-149"><strong>dbLangChineseTraditional</strong></span></span></p></td>
<td><p><span data-ttu-id="97b7c-150">Chinesisch (Traditionell)</span><span class="sxs-lookup"><span data-stu-id="97b7c-150">Traditional Chinese</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="97b7c-151"><strong>dbLangCyrillic</strong></span><span class="sxs-lookup"><span data-stu-id="97b7c-151"><strong>dbLangCyrillic</strong></span></span></p></td>
<td><p><span data-ttu-id="97b7c-152">Russisch</span><span class="sxs-lookup"><span data-stu-id="97b7c-152">Russian</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="97b7c-153"><strong>dbLangCzech</strong></span><span class="sxs-lookup"><span data-stu-id="97b7c-153"><strong>dbLangCzech</strong></span></span></p></td>
<td><p><span data-ttu-id="97b7c-154">Tschechisch</span><span class="sxs-lookup"><span data-stu-id="97b7c-154">Czech</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="97b7c-155"><strong>dbLangDutch</strong></span><span class="sxs-lookup"><span data-stu-id="97b7c-155"><strong>dbLangDutch</strong></span></span></p></td>
<td><p><span data-ttu-id="97b7c-156">Niederländisch</span><span class="sxs-lookup"><span data-stu-id="97b7c-156">Dutch</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="97b7c-157"><strong>dbLangGreek</strong></span><span class="sxs-lookup"><span data-stu-id="97b7c-157"><strong>dbLangGreek</strong></span></span></p></td>
<td><p><span data-ttu-id="97b7c-158">Griechisch</span><span class="sxs-lookup"><span data-stu-id="97b7c-158">Greek</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="97b7c-159"><strong>dbLangHebrew</strong></span><span class="sxs-lookup"><span data-stu-id="97b7c-159"><strong>dbLangHebrew</strong></span></span></p></td>
<td><p><span data-ttu-id="97b7c-160">Hebräisch</span><span class="sxs-lookup"><span data-stu-id="97b7c-160">Hebrew</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="97b7c-161"><strong>dbLangHungarian</strong></span><span class="sxs-lookup"><span data-stu-id="97b7c-161"><strong>dbLangHungarian</strong></span></span></p></td>
<td><p><span data-ttu-id="97b7c-162">Ungarisch</span><span class="sxs-lookup"><span data-stu-id="97b7c-162">Hungarian</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="97b7c-163"><strong>dbLangIcelandic</strong></span><span class="sxs-lookup"><span data-stu-id="97b7c-163"><strong>dbLangIcelandic</strong></span></span></p></td>
<td><p><span data-ttu-id="97b7c-164">Isländisch</span><span class="sxs-lookup"><span data-stu-id="97b7c-164">Icelandic</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="97b7c-165"><strong>dbLangJapanese</strong></span><span class="sxs-lookup"><span data-stu-id="97b7c-165"><strong>dbLangJapanese</strong></span></span></p></td>
<td><p><span data-ttu-id="97b7c-166">Japanisch</span><span class="sxs-lookup"><span data-stu-id="97b7c-166">Japanese</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="97b7c-167"><strong>dbLangKorean</strong></span><span class="sxs-lookup"><span data-stu-id="97b7c-167"><strong>dbLangKorean</strong></span></span></p></td>
<td><p><span data-ttu-id="97b7c-168">Koreanisch</span><span class="sxs-lookup"><span data-stu-id="97b7c-168">Korean</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="97b7c-169"><strong>dbLangNordic</strong></span><span class="sxs-lookup"><span data-stu-id="97b7c-169"><strong>dbLangNordic</strong></span></span></p></td>
<td><p><span data-ttu-id="97b7c-170">Nordeuropäische Sprachen (nur Version 1.0 des Microsoft Jet-Datenbankmoduls)</span><span class="sxs-lookup"><span data-stu-id="97b7c-170">Nordic languages (Microsoft Jet database engine version 1.0 only)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="97b7c-171"><strong>dbLangNorwDan</strong></span><span class="sxs-lookup"><span data-stu-id="97b7c-171"><strong>dbLangNorwDan</strong></span></span></p></td>
<td><p><span data-ttu-id="97b7c-172">Norwegisch und Dänisch</span><span class="sxs-lookup"><span data-stu-id="97b7c-172">Norwegian and Danish</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="97b7c-173"><strong>dbLangPolish</strong></span><span class="sxs-lookup"><span data-stu-id="97b7c-173"><strong>dbLangPolish</strong></span></span></p></td>
<td><p><span data-ttu-id="97b7c-174">Polnisch</span><span class="sxs-lookup"><span data-stu-id="97b7c-174">Polish</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="97b7c-175"><strong>dbLangSlovenian</strong></span><span class="sxs-lookup"><span data-stu-id="97b7c-175"><strong>dbLangSlovenian</strong></span></span></p></td>
<td><p><span data-ttu-id="97b7c-176">Slowenisch</span><span class="sxs-lookup"><span data-stu-id="97b7c-176">Slovenian</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="97b7c-177"><strong>dbLangSpanish</strong></span><span class="sxs-lookup"><span data-stu-id="97b7c-177"><strong>dbLangSpanish</strong></span></span></p></td>
<td><p><span data-ttu-id="97b7c-178">Spanisch (Traditionell)</span><span class="sxs-lookup"><span data-stu-id="97b7c-178">Traditional Spanish</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="97b7c-179"><strong>dbLangSwedFin</strong></span><span class="sxs-lookup"><span data-stu-id="97b7c-179"><strong>dbLangSwedFin</strong></span></span></p></td>
<td><p><span data-ttu-id="97b7c-180">Schwedisch und Finnisch</span><span class="sxs-lookup"><span data-stu-id="97b7c-180">Swedish and Finnish</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="97b7c-181"><strong>dbLangThai</strong></span><span class="sxs-lookup"><span data-stu-id="97b7c-181"><strong>dbLangThai</strong></span></span></p></td>
<td><p><span data-ttu-id="97b7c-182">Thailändisch</span><span class="sxs-lookup"><span data-stu-id="97b7c-182">Thai</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="97b7c-183"><strong>dbLangTurkish</strong></span><span class="sxs-lookup"><span data-stu-id="97b7c-183"><strong>dbLangTurkish</strong></span></span></p></td>
<td><p><span data-ttu-id="97b7c-184">Türkisch</span><span class="sxs-lookup"><span data-stu-id="97b7c-184">Turkish</span></span></p></td>
</tr>
</tbody>
</table>

<br/>

<span data-ttu-id="97b7c-185">Sie können eine oder mehrere der folgenden Konstanten im Argument options verwenden, um anzugeben, welche Version das Datenformat haben soll und ob die Datenbank verschlüsselt werden soll.</span><span class="sxs-lookup"><span data-stu-id="97b7c-185">You can use one or more of the following constants in the options argument to specify which version the data format should have and whether or not to encrypt the database.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="97b7c-186">Konstante</span><span class="sxs-lookup"><span data-stu-id="97b7c-186">Constant</span></span></p></th>
<th><p><span data-ttu-id="97b7c-187">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="97b7c-187">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="97b7c-188"><strong>dbEncrypt</strong></span><span class="sxs-lookup"><span data-stu-id="97b7c-188"><strong>dbEncrypt</strong></span></span></p></td>
<td><p><span data-ttu-id="97b7c-189">Erstellt eine verschlüsselte Datenbank.</span><span class="sxs-lookup"><span data-stu-id="97b7c-189">Creates an encrypted database.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="97b7c-190"><strong>dbVersion10</strong></span><span class="sxs-lookup"><span data-stu-id="97b7c-190"><strong>dbVersion10</strong></span></span></p></td>
<td><p><span data-ttu-id="97b7c-191">Erstellt eine Datenbank, die das Dateiformat der Version 1.0 des Microsoft Jet-Datenbankmoduls verwendet.</span><span class="sxs-lookup"><span data-stu-id="97b7c-191">Creates a database that uses the Microsoft Jet database engine version 1.0 file format.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="97b7c-192"><strong>dbVersion11</strong></span><span class="sxs-lookup"><span data-stu-id="97b7c-192"><strong>dbVersion11</strong></span></span></p></td>
<td><p><span data-ttu-id="97b7c-193">Erstellt eine Datenbank, die das Dateiformat der Version 1.1 des Microsoft Jet-Datenbankmoduls verwendet.</span><span class="sxs-lookup"><span data-stu-id="97b7c-193">Creates a database that uses the Microsoft Jet database engine version 1.1 file format.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="97b7c-194"><strong>dbVersion20</strong></span><span class="sxs-lookup"><span data-stu-id="97b7c-194"><strong>dbVersion20</strong></span></span></p></td>
<td><p><span data-ttu-id="97b7c-195">Erstellt eine Datenbank, die das Dateiformat der Version 2.0 des Microsoft Jet-Datenbankmoduls verwendet.</span><span class="sxs-lookup"><span data-stu-id="97b7c-195">Creates a database that uses the Microsoft Jet database engine version 2.0 file format.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="97b7c-196"><strong>dbVersion30</strong></span><span class="sxs-lookup"><span data-stu-id="97b7c-196"><strong>dbVersion30</strong></span></span></p></td>
<td><p><span data-ttu-id="97b7c-197">Erstellt eine Datenbank, die das Dateiformat der Version 3.0 des Microsoft Jet-Datenbankmoduls verwendet (kompatibel mit Version 3.5).</span><span class="sxs-lookup"><span data-stu-id="97b7c-197">Creates a database that uses the Microsoft Jet database engine version 3.0 file format (compatible with version 3.5).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="97b7c-198"><strong>dbVersion40</strong></span><span class="sxs-lookup"><span data-stu-id="97b7c-198"><strong>dbVersion40</strong></span></span></p></td>
<td><p><span data-ttu-id="97b7c-199">Erstellt eine Datenbank, die das Dateiformat der Version 4.0 des Microsoft Jet-Datenbankmoduls verwendet.</span><span class="sxs-lookup"><span data-stu-id="97b7c-199">Creates a database that uses the Microsoft Jet database engine version 4.0 file format.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="97b7c-200"><strong>dbVersion120</strong></span><span class="sxs-lookup"><span data-stu-id="97b7c-200"><strong>dbVersion120</strong></span></span></p></td>
<td><p><span data-ttu-id="97b7c-201">Erstellt eine Datenbank, die das Dateiformat der Version 12.0 des Microsoft Access-Datenbankmoduls verwendet.</span><span class="sxs-lookup"><span data-stu-id="97b7c-201">Creates a database that uses the Microsoft Access database engine version 12.0 file format.</span></span></p></td>
</tr>
</tbody>
</table>

<br/>

<span data-ttu-id="97b7c-202">Wenn Sie die Verschlüsselungskonstante weglassen, erstellt **CreateDatabase** eine nicht verschlüsselte Datenbank.</span><span class="sxs-lookup"><span data-stu-id="97b7c-202">If you omit the encryption constant, **CreateDatabase** creates an un-encrypted database.</span></span>

<span data-ttu-id="97b7c-p105">Verwenden Sie die **CreateDatabase**-Methode zum Erstellen und Öffnen einer neuen, leeren Datenbank, und geben Sie das **Database**-Objekt zurück. Mithilfe zusätzlicher DAO-Objekte müssen Sie dessen Struktur und Inhalt vollständig angeben. Wenn Sie eine vorhandene Datenbank teilweise oder vollständig kopieren möchten, können Sie unter Verwendung der **[CompactDatabase](dbengine-compactdatabase-method-dao.md)** -Methode eine Kopie erstellen und diese anpassen.</span><span class="sxs-lookup"><span data-stu-id="97b7c-p105">Use the **CreateDatabase** method to create and open a new, empty database, and return the **Database** object. You must complete its structure and content by using additional DAO objects. If you want to make a partial or complete copy of an existing database, you can use the **[CompactDatabase](dbengine-compactdatabase-method-dao.md)** method to make a copy that you can customize.</span></span>

## <a name="example"></a><span data-ttu-id="97b7c-206">Beispiel</span><span class="sxs-lookup"><span data-stu-id="97b7c-206">Example</span></span>

<span data-ttu-id="97b7c-207">In diesem Beispiel wird mithilfe von **CreateDatabase** ein neues, verschlüsseltes **Database**-Objekt erstellt.</span><span class="sxs-lookup"><span data-stu-id="97b7c-207">This example uses **CreateDatabase** to create a new, encrypted **Database** object.</span></span>

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
