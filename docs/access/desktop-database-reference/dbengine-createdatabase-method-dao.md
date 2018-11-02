---
title: DBEngine.CreateDatabase-Methode (DAO)
TOCTitle: CreateDatabase Method
ms:assetid: d5821a4b-483a-b8fa-e929-5f036057d8c4
ms:mtpsurl: https://msdn.microsoft.com/library/Ff835033(v=office.15)
ms:contentKeyID: 48547966
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052972
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 7478a06df491f4c2254f8c72f0eacf9c4b19d49e
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/02/2018
ms.locfileid: "25927508"
---
# <a name="dbenginecreatedatabase-method-dao"></a><span data-ttu-id="e1897-102">DBEngine.CreateDatabase-Methode (DAO)</span><span class="sxs-lookup"><span data-stu-id="e1897-102">DBEngine.CreateDatabase method (DAO)</span></span>


<span data-ttu-id="e1897-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="e1897-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="e1897-p101">Erstellt ein neues **[Database](database-object-dao.md)** -Objekt, speichert die Datenbank auf einem Datenträger und gibt ein geöffnetes **Database**-Objekt zurück (gilt nur für Microsoft Access-Arbeitsbereiche).</span><span class="sxs-lookup"><span data-stu-id="e1897-p101">Creates a new **[Database](database-object-dao.md)** object, saves the database to disk, and returns an opened **Database** object (Microsoft Access workspaces only). .</span></span>

## <a name="syntax"></a><span data-ttu-id="e1897-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="e1897-106">Syntax</span></span>

<span data-ttu-id="e1897-107">*Ausdruck* . CreateDatabase (***Name***, ***Gebietsschema***, ***Option***)</span><span class="sxs-lookup"><span data-stu-id="e1897-107">*expression* .CreateDatabase(***Name***, ***Locale***, ***Option***)</span></span>

<span data-ttu-id="e1897-108">*Ausdruck* Eine Variable, die ein **DBEngine** -Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="e1897-108">*expression* A variable that represents a **DBEngine** object.</span></span>

### <a name="parameters"></a><span data-ttu-id="e1897-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="e1897-109">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="e1897-110">Name</span><span class="sxs-lookup"><span data-stu-id="e1897-110">Name</span></span></p></th>
<th><p><span data-ttu-id="e1897-111">Erforderlich/Optional</span><span class="sxs-lookup"><span data-stu-id="e1897-111">Required/Optional</span></span></p></th>
<th><p><span data-ttu-id="e1897-112">Datentyp</span><span class="sxs-lookup"><span data-stu-id="e1897-112">Data Type</span></span></p></th>
<th><p><span data-ttu-id="e1897-113">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e1897-113">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e1897-114">Name</span><span class="sxs-lookup"><span data-stu-id="e1897-114">Name</span></span></p></td>
<td><p><span data-ttu-id="e1897-115">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="e1897-115">Required</span></span></p></td>
<td><p><span data-ttu-id="e1897-116"><strong>String</strong></span><span class="sxs-lookup"><span data-stu-id="e1897-116"><strong>String</strong></span></span></p></td>
<td><p><span data-ttu-id="e1897-117">Eine Zeichenfolge bis zu 255 Zeichen lang sein darf, die den Namen der Datenbankdatei ist, den Sie erstellen.</span><span class="sxs-lookup"><span data-stu-id="e1897-117">A String up to 255 characters long that is the name of the database file that you're creating.</span></span> <span data-ttu-id="e1897-118">Der vollständige Pfad und der Dateiname kann sein.</span><span class="sxs-lookup"><span data-stu-id="e1897-118">It can be the full path and file name.</span></span> <span data-ttu-id="e1897-119">Wenn Ihr Netzwerk unterstützt, Sie können auch angeben einen Netzwerkpfad wie &quot; \\server1\share1\dir1\db1&quot;.</span><span class="sxs-lookup"><span data-stu-id="e1897-119">If your network supports it, you can also specify a network path, such as &quot;\\server1\share1\dir1\db1&quot;.</span></span> <span data-ttu-id="e1897-120">Sie können mit dieser Methode nur Microsoft Access-Datenbankdateien erstellen.</span><span class="sxs-lookup"><span data-stu-id="e1897-120">You can only create Microsoft Access database files with this method.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e1897-121">Locale</span><span class="sxs-lookup"><span data-stu-id="e1897-121">Locale</span></span></p></td>
<td><p><span data-ttu-id="e1897-122">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="e1897-122">Required</span></span></p></td>
<td><p><span data-ttu-id="e1897-123"><strong>String</strong></span><span class="sxs-lookup"><span data-stu-id="e1897-123"><strong>String</strong></span></span></p></td>
<td><ul>
<li><p><span data-ttu-id="e1897-p103">Ein Zeichenfolgenausdruck, der eine Sortierreihenfolge zum Erstellen der Datenbank angibt, wie unter Einstellungen festgelegt. Wenn Sie dieses Argument nicht angeben, tritt ein Fehler auf.</span><span class="sxs-lookup"><span data-stu-id="e1897-p103">A string expression that specifies a collating order for creating the database, as specified in Settings. You must supply this argument or an error occurs.</span></span></p></li>
<li><p><span data-ttu-id="e1897-126">Sie können auch ein Kennwort für das neue <strong>Database</strong> -Objekt erstellen, indem Sie die Kennwortzeichenfolge (beginnend mit &quot;; Pwd =&quot; ) mit einer Konstante im Argument <em>Locale</em> verknüpfen, wie folgt:</span><span class="sxs-lookup"><span data-stu-id="e1897-126">You can also create a password for the new <strong>Database</strong> object by concatenating the password string (starting with &quot;;pwd=&quot; ) with a constant in the <em>locale</em> argument, like this:</span></span></p></li>
<li><p><span data-ttu-id="e1897-127">DbLangSpanish &amp; &quot;; Pwd = NewPassword&quot;</span><span class="sxs-lookup"><span data-stu-id="e1897-127">dbLangSpanish &amp; &quot;;pwd=NewPassword&quot;</span></span></p></li>
<li><p><span data-ttu-id="e1897-128">Wenn Sie das standardmäßige <em>locale</em> verwenden möchten, aber ein Kennwort angeben, geben Sie für das Argument <em>locale</em> einfach eine Kennwortzeichenfolge an:</span><span class="sxs-lookup"><span data-stu-id="e1897-128">If you want to use the default <em>locale</em>, but specify a password, simply enter a password string for the <em>locale</em> argument:</span></span></p></li>
<li><p><span data-ttu-id="e1897-129">&quot;; Pwd = NewPassword&quot;</span><span class="sxs-lookup"><span data-stu-id="e1897-129">&quot;;pwd=NewPassword&quot;</span></span></p></li>
<li><p><span data-ttu-id="e1897-p104">[!HINWEIS] Verwenden Sie sichere Kennwörter aus Groß- und Kleinbuchstaben, Zahlen und Symbolen. Unsichere Kennwörter enthalten keine Kombination dieser Elemente. Sicheres Kennwort: Y6dh!et5. Unsicheres Kennwort: Haus27. Verwenden Sie ein sicheres Kennwort, das Sie sich gut merken können, damit Sie es nicht aufschreiben müssen.</span><span class="sxs-lookup"><span data-stu-id="e1897-p104">Use strong passwords that combine upper- and lowercase letters, numbers, and symbols. Weak passwords don't mix these elements. Strong password: Y6dh!et5. Weak password: House27. Use a strong password that you can remember so that you don't have to write it down.</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e1897-135">Option</span><span class="sxs-lookup"><span data-stu-id="e1897-135">Option</span></span></p></td>
<td><p><span data-ttu-id="e1897-136">Optional</span><span class="sxs-lookup"><span data-stu-id="e1897-136">Optional</span></span></p></td>
<td><p><span data-ttu-id="e1897-137"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="e1897-137"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="e1897-p105">Eine Konstante oder eine Kombination aus Konstanten, die eine oder mehrere Optionen angibt, wie unter Einstellungen festgelegt. Sie können Optionen kombinieren, indem Sie die Summe der entsprechenden Konstanten bilden.</span><span class="sxs-lookup"><span data-stu-id="e1897-p105">A constant or combination of constants that indicates one or more options, as specified in Settings. You can combine options by summing the corresponding constants.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="e1897-140">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e1897-140">Remarks</span></span>

<span data-ttu-id="e1897-141">Sie können eine der folgenden Konstanten für das Argument locale verwenden, um die **[CollatingOrder](database-collatingorder-property-dao.md)**-Eigenschaft von Text für Zeichenfolgenvergleiche anzugeben.</span><span class="sxs-lookup"><span data-stu-id="e1897-141">You can use one of the following constants for the locale argument to specify the **[CollatingOrder](database-collatingorder-property-dao.md)** property of text for string comparisons.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="e1897-142">Konstante</span><span class="sxs-lookup"><span data-stu-id="e1897-142">Constant</span></span></p></th>
<th><p><span data-ttu-id="e1897-143">Sortierreihenfolge</span><span class="sxs-lookup"><span data-stu-id="e1897-143">Collating order</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e1897-144"><strong>dbLangGeneral</strong></span><span class="sxs-lookup"><span data-stu-id="e1897-144"><strong>dbLangGeneral</strong></span></span></p></td>
<td><p><span data-ttu-id="e1897-145">Englisch, Deutsch, Französisch, Portugiesisch, Italienisch und modernes Spanisch</span><span class="sxs-lookup"><span data-stu-id="e1897-145">English, German, French, Portuguese, Italian, and Modern Spanish</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e1897-146"><strong>dbLangArabic</strong></span><span class="sxs-lookup"><span data-stu-id="e1897-146"><strong>dbLangArabic</strong></span></span></p></td>
<td><p><span data-ttu-id="e1897-147">Arabisch</span><span class="sxs-lookup"><span data-stu-id="e1897-147">Arabic</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e1897-148"><strong>dbLangChineseSimplified</strong></span><span class="sxs-lookup"><span data-stu-id="e1897-148"><strong>dbLangChineseSimplified</strong></span></span></p></td>
<td><p><span data-ttu-id="e1897-149">Chinesisch (Vereinfacht)</span><span class="sxs-lookup"><span data-stu-id="e1897-149">Simplified Chinese</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e1897-150"><strong>dbLangChineseTraditional</strong></span><span class="sxs-lookup"><span data-stu-id="e1897-150"><strong>dbLangChineseTraditional</strong></span></span></p></td>
<td><p><span data-ttu-id="e1897-151">Chinesisch (Traditionell)</span><span class="sxs-lookup"><span data-stu-id="e1897-151">Traditional Chinese</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e1897-152"><strong>dbLangCyrillic</strong></span><span class="sxs-lookup"><span data-stu-id="e1897-152"><strong>dbLangCyrillic</strong></span></span></p></td>
<td><p><span data-ttu-id="e1897-153">Russisch</span><span class="sxs-lookup"><span data-stu-id="e1897-153">Russian</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e1897-154"><strong>dbLangCzech</strong></span><span class="sxs-lookup"><span data-stu-id="e1897-154"><strong>dbLangCzech</strong></span></span></p></td>
<td><p><span data-ttu-id="e1897-155">Tschechisch</span><span class="sxs-lookup"><span data-stu-id="e1897-155">Czech</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e1897-156"><strong>dbLangDutch</strong></span><span class="sxs-lookup"><span data-stu-id="e1897-156"><strong>dbLangDutch</strong></span></span></p></td>
<td><p><span data-ttu-id="e1897-157">Niederländisch</span><span class="sxs-lookup"><span data-stu-id="e1897-157">Dutch</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e1897-158"><strong>dbLangGreek</strong></span><span class="sxs-lookup"><span data-stu-id="e1897-158"><strong>dbLangGreek</strong></span></span></p></td>
<td><p><span data-ttu-id="e1897-159">Griechisch</span><span class="sxs-lookup"><span data-stu-id="e1897-159">Greek</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e1897-160"><strong>dbLangHebrew</strong></span><span class="sxs-lookup"><span data-stu-id="e1897-160"><strong>dbLangHebrew</strong></span></span></p></td>
<td><p><span data-ttu-id="e1897-161">Hebräisch</span><span class="sxs-lookup"><span data-stu-id="e1897-161">Hebrew</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e1897-162"><strong>dbLangHungarian</strong></span><span class="sxs-lookup"><span data-stu-id="e1897-162"><strong>dbLangHungarian</strong></span></span></p></td>
<td><p><span data-ttu-id="e1897-163">Ungarisch</span><span class="sxs-lookup"><span data-stu-id="e1897-163">Hungarian</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e1897-164"><strong>dbLangIcelandic</strong></span><span class="sxs-lookup"><span data-stu-id="e1897-164"><strong>dbLangIcelandic</strong></span></span></p></td>
<td><p><span data-ttu-id="e1897-165">Isländisch</span><span class="sxs-lookup"><span data-stu-id="e1897-165">Icelandic</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e1897-166"><strong>dbLangJapanese</strong></span><span class="sxs-lookup"><span data-stu-id="e1897-166"><strong>dbLangJapanese</strong></span></span></p></td>
<td><p><span data-ttu-id="e1897-167">Japanisch</span><span class="sxs-lookup"><span data-stu-id="e1897-167">Japanese</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e1897-168"><strong>dbLangKorean</strong></span><span class="sxs-lookup"><span data-stu-id="e1897-168"><strong>dbLangKorean</strong></span></span></p></td>
<td><p><span data-ttu-id="e1897-169">Koreanisch</span><span class="sxs-lookup"><span data-stu-id="e1897-169">Korean</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e1897-170"><strong>dbLangNordic</strong></span><span class="sxs-lookup"><span data-stu-id="e1897-170"><strong>dbLangNordic</strong></span></span></p></td>
<td><p><span data-ttu-id="e1897-171">Nordeuropäische Sprachen (nur Version 1.0 des Microsoft Jet-Datenbankmoduls)</span><span class="sxs-lookup"><span data-stu-id="e1897-171">Nordic languages (Microsoft Jet database engine version 1.0 only)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e1897-172"><strong>dbLangNorwDan</strong></span><span class="sxs-lookup"><span data-stu-id="e1897-172"><strong>dbLangNorwDan</strong></span></span></p></td>
<td><p><span data-ttu-id="e1897-173">Norwegisch und Dänisch</span><span class="sxs-lookup"><span data-stu-id="e1897-173">Norwegian and Danish</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e1897-174"><strong>dbLangPolish</strong></span><span class="sxs-lookup"><span data-stu-id="e1897-174"><strong>dbLangPolish</strong></span></span></p></td>
<td><p><span data-ttu-id="e1897-175">Polnisch</span><span class="sxs-lookup"><span data-stu-id="e1897-175">Polish</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e1897-176"><strong>dbLangSlovenian</strong></span><span class="sxs-lookup"><span data-stu-id="e1897-176"><strong>dbLangSlovenian</strong></span></span></p></td>
<td><p><span data-ttu-id="e1897-177">Slowenisch</span><span class="sxs-lookup"><span data-stu-id="e1897-177">Slovenian</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e1897-178"><strong>dbLangSpanish</strong></span><span class="sxs-lookup"><span data-stu-id="e1897-178"><strong>dbLangSpanish</strong></span></span></p></td>
<td><p><span data-ttu-id="e1897-179">Spanisch (Traditionell)</span><span class="sxs-lookup"><span data-stu-id="e1897-179">Traditional Spanish</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e1897-180"><strong>dbLangSwedFin</strong></span><span class="sxs-lookup"><span data-stu-id="e1897-180"><strong>dbLangSwedFin</strong></span></span></p></td>
<td><p><span data-ttu-id="e1897-181">Schwedisch und Finnisch</span><span class="sxs-lookup"><span data-stu-id="e1897-181">Swedish and Finnish</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e1897-182"><strong>dbLangThai</strong></span><span class="sxs-lookup"><span data-stu-id="e1897-182"><strong>dbLangThai</strong></span></span></p></td>
<td><p><span data-ttu-id="e1897-183">Thailändisch</span><span class="sxs-lookup"><span data-stu-id="e1897-183">Thai</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e1897-184"><strong>dbLangTurkish</strong></span><span class="sxs-lookup"><span data-stu-id="e1897-184"><strong>dbLangTurkish</strong></span></span></p></td>
<td><p><span data-ttu-id="e1897-185">Türkisch</span><span class="sxs-lookup"><span data-stu-id="e1897-185">Turkish</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="e1897-186">Sie können eine oder mehrere der folgenden Konstanten im Argument options verwenden, um anzugeben, welche Version das Datenformat haben soll und ob die Datenbank verschlüsselt werden soll.</span><span class="sxs-lookup"><span data-stu-id="e1897-186">You can use one or more of the following constants in the options argument to specify which version the data format should have and whether or not to encrypt the database.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="e1897-187">Konstante</span><span class="sxs-lookup"><span data-stu-id="e1897-187">Constant</span></span></p></th>
<th><p><span data-ttu-id="e1897-188">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e1897-188">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e1897-189"><strong>dbEncrypt</strong></span><span class="sxs-lookup"><span data-stu-id="e1897-189"><strong>dbEncrypt</strong></span></span></p></td>
<td><p><span data-ttu-id="e1897-190">Erstellt eine verschlüsselte Datenbank.</span><span class="sxs-lookup"><span data-stu-id="e1897-190">Creates an encrypted database.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e1897-191"><strong>dbVersion10</strong></span><span class="sxs-lookup"><span data-stu-id="e1897-191"><strong>dbVersion10</strong></span></span></p></td>
<td><p><span data-ttu-id="e1897-192">Erstellt eine Datenbank, die das Dateiformat der Version 1.0 des Microsoft Jet-Datenbankmoduls verwendet.</span><span class="sxs-lookup"><span data-stu-id="e1897-192">Creates a database that uses the Microsoft Jet database engine version 1.0 file format.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e1897-193"><strong>dbVersion11</strong></span><span class="sxs-lookup"><span data-stu-id="e1897-193"><strong>dbVersion11</strong></span></span></p></td>
<td><p><span data-ttu-id="e1897-194">Erstellt eine Datenbank, die das Dateiformat der Version 1.1 des Microsoft Jet-Datenbankmoduls verwendet.</span><span class="sxs-lookup"><span data-stu-id="e1897-194">Creates a database that uses the Microsoft Jet database engine version 1.1 file format.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e1897-195"><strong>dbVersion20</strong></span><span class="sxs-lookup"><span data-stu-id="e1897-195"><strong>dbVersion20</strong></span></span></p></td>
<td><p><span data-ttu-id="e1897-196">Erstellt eine Datenbank, die das Dateiformat der Version 2.0 des Microsoft Jet-Datenbankmoduls verwendet.</span><span class="sxs-lookup"><span data-stu-id="e1897-196">Creates a database that uses the Microsoft Jet database engine version 2.0 file format.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e1897-197"><strong>dbVersion30</strong></span><span class="sxs-lookup"><span data-stu-id="e1897-197"><strong>dbVersion30</strong></span></span></p></td>
<td><p><span data-ttu-id="e1897-198">Erstellt eine Datenbank, die das Dateiformat der Version 3.0 des Microsoft Jet-Datenbankmoduls verwendet (kompatibel mit Version 3.5).</span><span class="sxs-lookup"><span data-stu-id="e1897-198">Creates a database that uses the Microsoft Jet database engine version 3.0 file format (compatible with version 3.5).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e1897-199"><strong>dbVersion40</strong></span><span class="sxs-lookup"><span data-stu-id="e1897-199"><strong>dbVersion40</strong></span></span></p></td>
<td><p><span data-ttu-id="e1897-200">Erstellt eine Datenbank, die das Dateiformat der Version 4.0 des Microsoft Jet-Datenbankmoduls verwendet.</span><span class="sxs-lookup"><span data-stu-id="e1897-200">Creates a database that uses the Microsoft Jet database engine version 4.0 file format.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e1897-201"><strong>dbVersion120</strong></span><span class="sxs-lookup"><span data-stu-id="e1897-201"><strong>dbVersion120</strong></span></span></p></td>
<td><p><span data-ttu-id="e1897-202">Erstellt eine Datenbank, die das Dateiformat der Version 12.0 des Microsoft Access-Datenbankmoduls verwendet.</span><span class="sxs-lookup"><span data-stu-id="e1897-202">Creates a database that uses the Microsoft Access database engine version 12.0 file format.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="e1897-203">Wenn Sie die Verschlüsselungskonstante weglassen, erstellt **CreateDatabase** eine nicht verschlüsselte Datenbank.</span><span class="sxs-lookup"><span data-stu-id="e1897-203">If you omit the encryption constant, **CreateDatabase** creates an un-encrypted database.</span></span>

<span data-ttu-id="e1897-p106">Verwenden Sie die **CreateDatabase**-Methode zum Erstellen und Öffnen einer neuen, leeren Datenbank, und geben Sie das **Database**-Objekt zurück. Mithilfe zusätzlicher DAO-Objekte müssen Sie dessen Struktur und Inhalt vollständig angeben. Wenn Sie eine vorhandene Datenbank teilweise oder vollständig kopieren möchten, können Sie unter Verwendung der **[CompactDatabase](dbengine-compactdatabase-method-dao.md)** -Methode eine Kopie erstellen und diese anpassen.</span><span class="sxs-lookup"><span data-stu-id="e1897-p106">Use the **CreateDatabase** method to create and open a new, empty database, and return the **Database** object. You must complete its structure and content by using additional DAO objects. If you want to make a partial or complete copy of an existing database, you can use the **[CompactDatabase](dbengine-compactdatabase-method-dao.md)** method to make a copy that you can customize.</span></span>

