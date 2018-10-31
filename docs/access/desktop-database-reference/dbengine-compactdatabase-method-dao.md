---
title: DBEngine.CompactDatabase-Methode (DAO)
TOCTitle: CompactDatabase Method
ms:assetid: 03f3a156-005a-4b71-81b0-598f326f7d42
ms:mtpsurl: https://msdn.microsoft.com/library/Ff844821(v=office.15)
ms:contentKeyID: 48542997
ms.date: 10/24/2016
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052936
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 9452a76f9e5d467279ee427c6c07016107833acf
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "25861432"
---
# <a name="dbenginecompactdatabase-method-dao"></a><span data-ttu-id="1353f-102">DBEngine.CompactDatabase-Methode (DAO)</span><span class="sxs-lookup"><span data-stu-id="1353f-102">DBEngine.CompactDatabase Method (DAO)</span></span>

<span data-ttu-id="1353f-103">**Betrifft**: Access 2013 | Access 2016</span><span class="sxs-lookup"><span data-stu-id="1353f-103">**Applies to**: Access 2013 | Access 2016</span></span>

<span data-ttu-id="1353f-104">Kopiert und komprimiert eine geschlossene Datenbank und bietet Ihnen die Möglichkeit, ihre Version, Sortierreihenfolge und Verschlüsselung.</span><span class="sxs-lookup"><span data-stu-id="1353f-104">Copies and compacts a closed database, and gives you the option of changing its version, collating order, and encryption.</span></span> <span data-ttu-id="1353f-105">(Nur Microsoft Access-Arbeitsbereiche).</span><span class="sxs-lookup"><span data-stu-id="1353f-105">(Microsoft Access workspaces only).</span></span>

> [!NOTE]
> <span data-ttu-id="1353f-106">Wenn Sie verschlüsselte verknüpfte Tabellen für die Aktion, Update und SQL-Abfragen [wie eine SQL UPDATE-Anweisung (CurrentDb.Execute "Aktualisieren...")] zu verwenden, müssen Sie den Verschlüsselungsschlüssel angeben.</span><span class="sxs-lookup"><span data-stu-id="1353f-106">When using encrypted linked tables for action, update, and SQL queries [such as a SQL UPDATE statement (CurrentDb.Execute "UPDATE...")], you must supply the encryption key.</span></span> <span data-ttu-id="1353f-107">Darüber hinaus sind verknüpfte Tabellen 19-Zeichen beschränkt für den Verschlüsselungsschlüssel.</span><span class="sxs-lookup"><span data-stu-id="1353f-107">Also, linked tables have a 19-character limit for the encryption key.</span></span> <span data-ttu-id="1353f-108">Finden Sie im Abschnitt **verschlüsselte verknüpfte Tabellen** am Ende dieses Themas.</span><span class="sxs-lookup"><span data-stu-id="1353f-108">See the **Encrypted linked tables** section at the end of this topic.</span></span>

## <a name="syntax"></a><span data-ttu-id="1353f-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="1353f-109">Syntax</span></span>

<span data-ttu-id="1353f-110">*Ausdruck* . CompactDatabase (***SrcName***, ***DstName***, ***DstLocale***, ***Optionen***, ***Kennwort***)</span><span class="sxs-lookup"><span data-stu-id="1353f-110">*expression* .CompactDatabase(***SrcName***, ***DstName***, ***DstLocale***, ***Options***, ***password***)</span></span>

<span data-ttu-id="1353f-111">*Ausdruck* Ein Ausdruck, der ein **DBEngine** -Objekt zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="1353f-111">*expression* An expression that returns a **DBEngine** object.</span></span>

### <a name="parameters"></a><span data-ttu-id="1353f-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="1353f-112">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="1353f-113">Name</span><span class="sxs-lookup"><span data-stu-id="1353f-113">Name</span></span></p></th>
<th><p><span data-ttu-id="1353f-114">Erforderlich/Optional</span><span class="sxs-lookup"><span data-stu-id="1353f-114">Required/Optional</span></span></p></th>
<th><p><span data-ttu-id="1353f-115">Datentyp</span><span class="sxs-lookup"><span data-stu-id="1353f-115">Data Type</span></span></p></th>
<th><p><span data-ttu-id="1353f-116">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="1353f-116">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="1353f-117">SrcName</span><span class="sxs-lookup"><span data-stu-id="1353f-117">SrcName</span></span></p></td>
<td><p><span data-ttu-id="1353f-118">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="1353f-118">Required</span></span></p></td>
<td><p><span data-ttu-id="1353f-119"><strong>Zeichenfolge</strong></span><span class="sxs-lookup"><span data-stu-id="1353f-119"><strong>String</strong></span></span></p></td>
<td><p><span data-ttu-id="1353f-120">Gibt eine vorhandene geschlossene Datenbank an.</span><span class="sxs-lookup"><span data-stu-id="1353f-120">Identifies an existing, closed database.</span></span> <span data-ttu-id="1353f-121">Sie können einen vollständigen Pfad und Dateinamen, wie etwa werden &quot;C:\db1.mdb&quot;.</span><span class="sxs-lookup"><span data-stu-id="1353f-121">It can be a full path and file name, such as &quot;C:\db1.mdb&quot;.</span></span> <span data-ttu-id="1353f-122">Wenn der Dateiname eine Erweiterung aufweist, müssen Sie es angeben.</span><span class="sxs-lookup"><span data-stu-id="1353f-122">If the file name has an extension, you must specify it.</span></span> <span data-ttu-id="1353f-123">Wenn Ihr Netzwerk unterstützt, Sie können auch angeben einen Netzwerkpfad wie &quot; \\server1\share1\dir1\db1.mdb&quot;</span><span class="sxs-lookup"><span data-stu-id="1353f-123">If your network supports it, you can also specify a network path, such as &quot;\\server1\share1\dir1\db1.mdb&quot;</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1353f-124">DstName</span><span class="sxs-lookup"><span data-stu-id="1353f-124">DstName</span></span></p></td>
<td><p><span data-ttu-id="1353f-125">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="1353f-125">Required</span></span></p></td>
<td><p><span data-ttu-id="1353f-126"><strong>Zeichenfolge</strong></span><span class="sxs-lookup"><span data-stu-id="1353f-126"><strong>String</strong></span></span></p></td>
<td><p><span data-ttu-id="1353f-p104">Der Dateiname (und Pfad) der komprimierten Datenbank, die Sie erstellen. Sie können auch einen Netzwerkpfad angeben. Mit diesem Argument kann nicht die gleiche Datenbankdatei angegeben werden wie mit SrcName.</span><span class="sxs-lookup"><span data-stu-id="1353f-p104">the file name (and path) of the compacted database that you're creating. You can also specify a network path. You can't use this argument to specify the same database file as SrcName.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1353f-130">DstLocale</span><span class="sxs-lookup"><span data-stu-id="1353f-130">DstLocale</span></span></p></td>
<td><p><span data-ttu-id="1353f-131">Optional</span><span class="sxs-lookup"><span data-stu-id="1353f-131">Optional</span></span></p></td>
<td><p><span data-ttu-id="1353f-132"><strong>Variante</strong></span><span class="sxs-lookup"><span data-stu-id="1353f-132"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="1353f-133">Ein Zeichenfolgenausdruck, der eine Sortierreihenfolge zum Erstellen von DstName angibt, wie unter „Hinweise" angegeben.</span><span class="sxs-lookup"><span data-stu-id="1353f-133">A string expression that specifies a collating order for creating DstName, as specified in Remarks.</span></span></p>
<ul>
<li><p><span data-ttu-id="1353f-134">Wenn Sie dieses Argument weglassen, hat DstName das gleiche Gebietsschema wie SrcName.</span><span class="sxs-lookup"><span data-stu-id="1353f-134">If you omit this argument, the locale of DstName is the same as SrcName.</span></span></p></li>
<li><p><span data-ttu-id="1353f-135">Sie können auch ein Kennwort für DstName erstellen, indem Sie die Kennwortzeichenfolge (beginnend mit &quot;; Pwd =&quot;) mit einer Konstante im Argument DstLocale wie folgt: DbLangSpanish &amp; &quot;; Pwd = NewPassword&quot;.</span><span class="sxs-lookup"><span data-stu-id="1353f-135">You can also create a password for DstName by concatenating the password string (starting with &quot;;pwd=&quot;) with a constant in the DstLocale argument, like this: dbLangSpanish &amp; &quot;;pwd=NewPassword&quot;.</span></span></p></li>
<li><p><span data-ttu-id="1353f-136">Wenn Sie dasselbe DstLocale wie SrcName (Standardwert) verwenden, aber ein neues Kennwort angeben möchten, geben Sie einfach eine Kennwortzeichenfolge für DstLocale ein: &quot;; Pwd = NewPassword&quot;</span><span class="sxs-lookup"><span data-stu-id="1353f-136">If you want to use the same DstLocale as SrcName (the default value), but specify a new password, simply enter a password string for DstLocale: &quot;;pwd=NewPassword&quot;</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1353f-137">Options</span><span class="sxs-lookup"><span data-stu-id="1353f-137">Options</span></span></p></td>
<td><p><span data-ttu-id="1353f-138">Optional</span><span class="sxs-lookup"><span data-stu-id="1353f-138">Optional</span></span></p></td>
<td><p><span data-ttu-id="1353f-139"><strong>Variante</strong></span><span class="sxs-lookup"><span data-stu-id="1353f-139"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="1353f-p105">Optional. Ein Konstante oder Kombination aus Konstanten, mit der mindestens eine Option angegeben wird, wie unter „Hinweise" angegeben. Sie können Optionen durch Summieren der entsprechenden Konstanten kombinieren.</span><span class="sxs-lookup"><span data-stu-id="1353f-p105">Optional. A constant or combination of constants that indicates one or more options, as specified in Remarks. You can combine options by summing the corresponding constants.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1353f-143">password</span><span class="sxs-lookup"><span data-stu-id="1353f-143">password</span></span></p></td>
<td><p><span data-ttu-id="1353f-144">Optional</span><span class="sxs-lookup"><span data-stu-id="1353f-144">Optional</span></span></p></td>
<td><p><span data-ttu-id="1353f-145"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="1353f-145"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="1353f-146">Ein Zeichenfolgenausdruck, einen Verschlüsselungsschlüssel enthält, wenn die Datenbank verschlüsselt ist.</span><span class="sxs-lookup"><span data-stu-id="1353f-146">A string expression containing an encryption key, if the database is encrypted.</span></span> <span data-ttu-id="1353f-147">Die Zeichenfolge &quot;; Pwd =&quot; dem tatsächlichen Kennwort vorausgehen muss.</span><span class="sxs-lookup"><span data-stu-id="1353f-147">The string &quot;;pwd=&quot; must precede the actual password.</span></span> <span data-ttu-id="1353f-148">Wenn Sie eine Kennworteinstellung in DstLocale einschließen, wird diese Einstellung ignoriert.</span><span class="sxs-lookup"><span data-stu-id="1353f-148">If you include a password setting in DstLocale, this setting is ignored.</span></span></p>

> [!NOTE]
> <span data-ttu-id="1353f-149">Dies ist veraltete Parameter und wird nicht unterstützt. ACCDB-Format.</span><span class="sxs-lookup"><span data-stu-id="1353f-149">This is deprecated parameter and is not supported in .ACCDB format.</span></span> <span data-ttu-id="1353f-150">Zum Verschlüsseln von ein. ACCDB-Datei, verwenden Sie die "Pwd =" option Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="1353f-150">To encrypt an .ACCDB file, use the "pwd=" option string.</span></span> <span data-ttu-id="1353f-151">[!HINWEIS] Verwenden Sie sichere Kennwörter aus Groß- und Kleinbuchstaben, Zahlen und Symbolen.</span><span class="sxs-lookup"><span data-stu-id="1353f-151">Use strong passwords that combine upper- and lowercase letters, numbers, and symbols.</span></span> <span data-ttu-id="1353f-152">Unsichere Kennwörter enthalten keine Kombination dieser Elemente.</span><span class="sxs-lookup"><span data-stu-id="1353f-152">Weak passwords don't mix these elements.</span></span> <span data-ttu-id="1353f-153">Sicheres Kennwort: Y6dh!et5.</span><span class="sxs-lookup"><span data-stu-id="1353f-153">Strong password: Y6dh!et5.</span></span> <span data-ttu-id="1353f-154">Unsicheres Kennwort: Haus27.</span><span class="sxs-lookup"><span data-stu-id="1353f-154">Weak password: House27.</span></span> <span data-ttu-id="1353f-155">Verwenden Sie ein sicheres Kennwort, das Sie sich gut merken können, damit Sie es nicht aufschreiben müssen.</span><span class="sxs-lookup"><span data-stu-id="1353f-155">Use a strong password that you can remember so that you don't have to write it down.</span></span>


</td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="1353f-156">Hinweise</span><span class="sxs-lookup"><span data-stu-id="1353f-156">Remarks</span></span>

<span data-ttu-id="1353f-157">Sie können eine der folgenden Konstanten für das DstLocale-Argument verwenden, um die **CollatingOrder** -Eigenschaft für Zeichenfolgenvergleiche von Text anzugeben.</span><span class="sxs-lookup"><span data-stu-id="1353f-157">You can use one of the following constants for the DstLocale argument to specify the **CollatingOrder** property for string comparisons of text.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="1353f-158">Konstante</span><span class="sxs-lookup"><span data-stu-id="1353f-158">Constant</span></span></p></th>
<th><p><span data-ttu-id="1353f-159">Sortierreihenfolge</span><span class="sxs-lookup"><span data-stu-id="1353f-159">Collating order</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="1353f-160"><strong>dbLangGeneral</strong></span><span class="sxs-lookup"><span data-stu-id="1353f-160"><strong>dbLangGeneral</strong></span></span></p></td>
<td><p><span data-ttu-id="1353f-161">Englisch, Deutsch, Französisch, Portugiesisch, Italienisch und modernes Spanisch</span><span class="sxs-lookup"><span data-stu-id="1353f-161">English, German, French, Portuguese, Italian, and Modern Spanish</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1353f-162"><strong>dbLangArabic</strong></span><span class="sxs-lookup"><span data-stu-id="1353f-162"><strong>dbLangArabic</strong></span></span></p></td>
<td><p><span data-ttu-id="1353f-163">Arabisch</span><span class="sxs-lookup"><span data-stu-id="1353f-163">Arabic</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1353f-164"><strong>dbLangChineseSimplified</strong></span><span class="sxs-lookup"><span data-stu-id="1353f-164"><strong>dbLangChineseSimplified</strong></span></span></p></td>
<td><p><span data-ttu-id="1353f-165">Chinesisch (Vereinfacht)</span><span class="sxs-lookup"><span data-stu-id="1353f-165">Simplified Chinese</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1353f-166"><strong>dbLangChineseTraditional</strong></span><span class="sxs-lookup"><span data-stu-id="1353f-166"><strong>dbLangChineseTraditional</strong></span></span></p></td>
<td><p><span data-ttu-id="1353f-167">Chinesisch (Traditionell)</span><span class="sxs-lookup"><span data-stu-id="1353f-167">Traditional Chinese</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1353f-168"><strong>dbLangCyrillic</strong></span><span class="sxs-lookup"><span data-stu-id="1353f-168"><strong>dbLangCyrillic</strong></span></span></p></td>
<td><p><span data-ttu-id="1353f-169">Russisch</span><span class="sxs-lookup"><span data-stu-id="1353f-169">Russian</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1353f-170"><strong>dbLangCzech</strong></span><span class="sxs-lookup"><span data-stu-id="1353f-170"><strong>dbLangCzech</strong></span></span></p></td>
<td><p><span data-ttu-id="1353f-171">Tschechisch</span><span class="sxs-lookup"><span data-stu-id="1353f-171">Czech</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1353f-172"><strong>dbLangDutch</strong></span><span class="sxs-lookup"><span data-stu-id="1353f-172"><strong>dbLangDutch</strong></span></span></p></td>
<td><p><span data-ttu-id="1353f-173">Niederländisch</span><span class="sxs-lookup"><span data-stu-id="1353f-173">Dutch</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1353f-174"><strong>dbLangGreek</strong></span><span class="sxs-lookup"><span data-stu-id="1353f-174"><strong>dbLangGreek</strong></span></span></p></td>
<td><p><span data-ttu-id="1353f-175">Griechisch</span><span class="sxs-lookup"><span data-stu-id="1353f-175">Greek</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1353f-176"><strong>dbLangHebrew</strong></span><span class="sxs-lookup"><span data-stu-id="1353f-176"><strong>dbLangHebrew</strong></span></span></p></td>
<td><p><span data-ttu-id="1353f-177">Hebräisch</span><span class="sxs-lookup"><span data-stu-id="1353f-177">Hebrew</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1353f-178"><strong>dbLangHungarian</strong></span><span class="sxs-lookup"><span data-stu-id="1353f-178"><strong>dbLangHungarian</strong></span></span></p></td>
<td><p><span data-ttu-id="1353f-179">Ungarisch</span><span class="sxs-lookup"><span data-stu-id="1353f-179">Hungarian</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1353f-180"><strong>dbLangIcelandic</strong></span><span class="sxs-lookup"><span data-stu-id="1353f-180"><strong>dbLangIcelandic</strong></span></span></p></td>
<td><p><span data-ttu-id="1353f-181">Isländisch</span><span class="sxs-lookup"><span data-stu-id="1353f-181">Icelandic</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1353f-182"><strong>dbLangJapanese</strong></span><span class="sxs-lookup"><span data-stu-id="1353f-182"><strong>dbLangJapanese</strong></span></span></p></td>
<td><p><span data-ttu-id="1353f-183">Japanisch</span><span class="sxs-lookup"><span data-stu-id="1353f-183">Japanese</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1353f-184"><strong>dbLangKorean</strong></span><span class="sxs-lookup"><span data-stu-id="1353f-184"><strong>dbLangKorean</strong></span></span></p></td>
<td><p><span data-ttu-id="1353f-185">Koreanisch</span><span class="sxs-lookup"><span data-stu-id="1353f-185">Korean</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1353f-186"><strong>dbLangNordic</strong></span><span class="sxs-lookup"><span data-stu-id="1353f-186"><strong>dbLangNordic</strong></span></span></p></td>
<td><p><span data-ttu-id="1353f-187">Nordeuropäische Sprachen (nur Version 1.0 des Microsoft Jet-Datenbankmoduls)</span><span class="sxs-lookup"><span data-stu-id="1353f-187">Nordic languages (Microsoft Jet database engine version 1.0 only)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1353f-188"><strong>dbLangNorwDan</strong></span><span class="sxs-lookup"><span data-stu-id="1353f-188"><strong>dbLangNorwDan</strong></span></span></p></td>
<td><p><span data-ttu-id="1353f-189">Norwegisch und Dänisch</span><span class="sxs-lookup"><span data-stu-id="1353f-189">Norwegian and Danish</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1353f-190"><strong>dbLangPolish</strong></span><span class="sxs-lookup"><span data-stu-id="1353f-190"><strong>dbLangPolish</strong></span></span></p></td>
<td><p><span data-ttu-id="1353f-191">Polnisch</span><span class="sxs-lookup"><span data-stu-id="1353f-191">Polish</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1353f-192"><strong>dbLangSlovenian</strong></span><span class="sxs-lookup"><span data-stu-id="1353f-192"><strong>dbLangSlovenian</strong></span></span></p></td>
<td><p><span data-ttu-id="1353f-193">Slowenisch</span><span class="sxs-lookup"><span data-stu-id="1353f-193">Slovenian</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1353f-194"><strong>dbLangSpanish</strong></span><span class="sxs-lookup"><span data-stu-id="1353f-194"><strong>dbLangSpanish</strong></span></span></p></td>
<td><p><span data-ttu-id="1353f-195">Spanisch (Traditionell)</span><span class="sxs-lookup"><span data-stu-id="1353f-195">Traditional Spanish</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1353f-196"><strong>dbLangSwedFin</strong></span><span class="sxs-lookup"><span data-stu-id="1353f-196"><strong>dbLangSwedFin</strong></span></span></p></td>
<td><p><span data-ttu-id="1353f-197">Schwedisch und Finnisch</span><span class="sxs-lookup"><span data-stu-id="1353f-197">Swedish and Finnish</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1353f-198"><strong>dbLangThai</strong></span><span class="sxs-lookup"><span data-stu-id="1353f-198"><strong>dbLangThai</strong></span></span></p></td>
<td><p><span data-ttu-id="1353f-199">Thailändisch</span><span class="sxs-lookup"><span data-stu-id="1353f-199">Thai</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1353f-200"><strong>dbLangTurkish</strong></span><span class="sxs-lookup"><span data-stu-id="1353f-200"><strong>dbLangTurkish</strong></span></span></p></td>
<td><p><span data-ttu-id="1353f-201">Türkisch</span><span class="sxs-lookup"><span data-stu-id="1353f-201">Turkish</span></span></p></td>
</tr>
</tbody>
</table>

<br/>

<span data-ttu-id="1353f-202">Sie können eine der folgenden Konstanten im options-Argument verwenden, um anzugeben, ob die Datenbank während der Komprimierung verschlüsselt werden soll.</span><span class="sxs-lookup"><span data-stu-id="1353f-202">You can use one of the following constants in the options argument to specify whether to encrypt or to decrypt the database while it's compacted.</span></span>

> [!NOTE]
> <span data-ttu-id="1353f-203">Die Konstanten DbEncrypt und DbDecrypt sind veraltet und nicht unterstützt. ACCDB-Dateiformate.</span><span class="sxs-lookup"><span data-stu-id="1353f-203">The constants dbEncrypt and dbDecrypt are deprecated and not supported in .ACCDB file formats.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="1353f-204">Konstante</span><span class="sxs-lookup"><span data-stu-id="1353f-204">Constant</span></span></p></th>
<th><p><span data-ttu-id="1353f-205">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="1353f-205">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="1353f-206"><strong>dbEncrypt</strong></span><span class="sxs-lookup"><span data-stu-id="1353f-206"><strong>dbEncrypt</strong></span></span></p></td>
<td><p><span data-ttu-id="1353f-207">Verschlüsselt die Datenbank beim Komprimieren.</span><span class="sxs-lookup"><span data-stu-id="1353f-207">Encrypt the database while compacting.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1353f-208"><strong>dbDecrypt</strong></span><span class="sxs-lookup"><span data-stu-id="1353f-208"><strong>dbDecrypt</strong></span></span></p></td>
<td><p><span data-ttu-id="1353f-209">Entschlüsselt die Datenbank beim Komprimieren.</span><span class="sxs-lookup"><span data-stu-id="1353f-209">Decrypt the database while compacting.</span></span></p></td>
</tr>
</tbody>
</table>

<br/>

<span data-ttu-id="1353f-210">Wenn Sie keine Verschlüsselungskonstante angeben, oder wenn Sie sowohl **DbDecrypt** als auch **DbEncrypt** einschließen, hat DstName die gleiche Verschlüsselung wie SrcName.</span><span class="sxs-lookup"><span data-stu-id="1353f-210">If you omit an encryption constant or if you include both **dbDecrypt** and **dbEncrypt**, DstName will have the same encryption as SrcName.</span></span>

<span data-ttu-id="1353f-p108">Sie können eine der folgenden Konstanten im options-Argument verwenden, um die Version des Datenformats für die komprimierte Datenbank anzugeben. Diese Konstante betrifft nur die Version des Datenformats von DstName und hat keine Auswirkungen auf die Version von von Microsoft Access definierten Objekten, wie Formulare und Berichte.</span><span class="sxs-lookup"><span data-stu-id="1353f-p108">You can use one of the following constants in the options argument to specify the version of the data format for the compacted database. This constant affects only the version of the data format of DstName and doesn't affect the version of any Microsoft Access-defined objects, such as forms and reports.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="1353f-213">Konstante</span><span class="sxs-lookup"><span data-stu-id="1353f-213">Constant</span></span></p></th>
<th><p><span data-ttu-id="1353f-214">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="1353f-214">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="1353f-215"><strong>dbVersion10</strong></span><span class="sxs-lookup"><span data-stu-id="1353f-215"><strong>dbVersion10</strong></span></span></p></td>
<td><p><span data-ttu-id="1353f-216">Erstellt eine Datenbank, die beim Komprimieren das Dateiformat der Version 1.0 des Microsoft Jet-Datenbankmoduls verwendet.</span><span class="sxs-lookup"><span data-stu-id="1353f-216">Creates a database that uses the Microsoft Jet database engine version 1.0 file format while compacting.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1353f-217"><strong>dbVersion11</strong></span><span class="sxs-lookup"><span data-stu-id="1353f-217"><strong>dbVersion11</strong></span></span></p></td>
<td><p><span data-ttu-id="1353f-218">Erstellt eine Datenbank, die beim Komprimieren das Dateiformat der Version 1.1 des Microsoft Jet-Datenbankmoduls verwendet.</span><span class="sxs-lookup"><span data-stu-id="1353f-218">Creates a database that uses the Microsoft Jet database engine version 1.1 file format while compacting.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1353f-219"><strong>dbVersion20</strong></span><span class="sxs-lookup"><span data-stu-id="1353f-219"><strong>dbVersion20</strong></span></span></p></td>
<td><p><span data-ttu-id="1353f-220">Erstellt eine Datenbank, die beim Komprimieren das Dateiformat der Version 2.0 des Microsoft Jet-Datenbankmoduls verwendet.</span><span class="sxs-lookup"><span data-stu-id="1353f-220">Creates a database that uses the Microsoft Jet database engine version 2.0 file format while compacting.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1353f-221"><strong>dbVersion30</strong></span><span class="sxs-lookup"><span data-stu-id="1353f-221"><strong>dbVersion30</strong></span></span></p></td>
<td><p><span data-ttu-id="1353f-222">Erstellt eine Datenbank, die beim Komprimieren das Dateiformat der Version 3.0 des Microsoft Jet-Datenbankmoduls (kompatibel mit Version 3.5) verwendet.</span><span class="sxs-lookup"><span data-stu-id="1353f-222">Creates a database that uses the Microsoft Jet database engine version 3.0 file format (compatible with version 3.5) while compacting.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1353f-223"><strong>dbVersion40</strong></span><span class="sxs-lookup"><span data-stu-id="1353f-223"><strong>dbVersion40</strong></span></span></p></td>
<td><p><span data-ttu-id="1353f-224">Erstellt eine Datenbank, die beim Komprimieren das Dateiformat der Version 4.0 des Microsoft Jet-Datenbankmoduls verwendet.</span><span class="sxs-lookup"><span data-stu-id="1353f-224">Creates a database that uses the Microsoft Jet database engine version 4.0 file format while compacting.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1353f-225"><strong>dbVersion120</strong></span><span class="sxs-lookup"><span data-stu-id="1353f-225"><strong>dbVersion120</strong></span></span></p></td>
<td><p><span data-ttu-id="1353f-226">Erstellt eine Datenbank, die beim Komprimieren das Dateiformat der Version 12.0 des Microsoft Access-Datenbankmoduls verwendet.</span><span class="sxs-lookup"><span data-stu-id="1353f-226">Creates a database that uses the Microsoft Access database engine version 12.0 file format while compacting.</span></span></p></td>
</tr>
</tbody>
</table>

<br/>

<span data-ttu-id="1353f-p109">Sie können nur eine Versionskonstante angeben. Wenn Sie keine Versionskonstante angeben, hat DstName die gleiche Version wie SrcName. Sie können DstName nur auf eine Version komprimieren, die der von SrcName entspricht oder höher ist.</span><span class="sxs-lookup"><span data-stu-id="1353f-p109">You can specify only one version constant. If you omit a version constant, DstName will have the same version as SrcName. You can compact DstName only to a version that is the same or later than that of SrcName.</span></span>

<span data-ttu-id="1353f-p110">Wenn Sie Daten in einer Datenbank ändern, kann die Datenbankdatei fragmentiert werden und mehr Speicherplatz belegen als erforderlich. Sie können die Datenbank in regelmäßigen Abständen mit der **CompactDatabase** -Methode komprimieren, um die Datenbankdatei zu defragmentieren. Die komprimierte Datenbank ist in der Regel kleiner und wird oft schneller ausgeführt. Sie können auch die Sortierreihenfolge, die Verschlüsselung oder die Version des Datenformats ändern, während Sie die Datenbank kopieren und komprimieren.</span><span class="sxs-lookup"><span data-stu-id="1353f-p110">As you change data in a database, the database file can become fragmented and use more disk space than is necessary. Periodically, you can use the **CompactDatabase** method to compact your database to defragment the database file. The compacted database is usually smaller and often runs faster. You can also change the collating order, the encryption, or the version of the data format while you copy and compact the database.</span></span>

<span data-ttu-id="1353f-p111">Sie müssen SrcName schließen, bevor Sie die Datenbank komprimieren. In einer Mehrbenutzerumgebung darf SrcName während der Komprimierung nicht von einem anderen Benutzer geöffnet sein. Wenn SrcName nicht geschlossen oder nicht für die exklusive Verwendung verfügbar ist, tritt ein Fehler auf.</span><span class="sxs-lookup"><span data-stu-id="1353f-p111">You must close SrcName before you compact it. In a multiuser environment, other users can't have SrcName open while you're compacting it. If SrcName isn't closed or isn't available for exclusive use, an error occurs.</span></span>

<span data-ttu-id="1353f-p112">Da **CompactDatabase** eine Kopie der Datenbank erstellt, muss genügend Speicherplatz für das Original und die Kopie der Datenbank vorhanden sein. Wenn nicht genügend Speicherplatz vorhanden ist, tritt bei der Komprimierung ein Fehler auf. Die Kopie der DstName-Datenbank muss sich nicht auf demselben Datenträger wie SrcName befinden. Nach erfolgreicher Komprimierung einer Datenbank können Sie die SrcName-Datei löschen und die komprimierte DstName-Datei in den ursprünglichen Dateinamen umbenennen.</span><span class="sxs-lookup"><span data-stu-id="1353f-p112">Because **CompactDatabase** creates a copy of the database, you must have enough disk space for both the original and the duplicate databases. The compact operation fails if there isn't enough disk space available. The DstName duplicate database doesn't have to be on the same disk as SrcName. After successfully compacting a database, you can delete the SrcName file and rename the compacted DstName file to the original file name.</span></span>

<span data-ttu-id="1353f-241">Die **CompactDatabase** -Methode kopiert alle Daten und die Einstellungen für die Sicherheitsberechtigung aus der durch SrcName angegebenen Datenbank in die durch DstName angegebene Datenbank.</span><span class="sxs-lookup"><span data-stu-id="1353f-241">The **CompactDatabase** method copies all the data and the security permission settings from the database specified by SrcName to the database specified by DstName.</span></span>

> [!NOTE]
> <span data-ttu-id="1353f-242">[!HINWEIS] Da die **CompactDatabase** -Methode keine Microsoft Access-Objekte konvertiert, sollten Sie **CompactDatabase** nicht zum Konvertieren einer Datenbank verwenden, die solche Objekte enthält.</span><span class="sxs-lookup"><span data-stu-id="1353f-242">Because the **CompactDatabase** method doesn't convert Microsoft Access objects, you shouldn't use **CompactDatabase** to convert a database containing such objects.</span></span>

## <a name="encrypted-linked-tables"></a><span data-ttu-id="1353f-243">Verschlüsselte verknüpfte Tabellen</span><span class="sxs-lookup"><span data-stu-id="1353f-243">Encrypted linked tables</span></span>

<span data-ttu-id="1353f-p113">Verschlüsselte Kennwörter sind vom Dateiformat der Datenbank, die Sie verwenden, abhängig. Wenn Sie eine Access 2003 (.mdb) oder frühere Version der Datenbank verwenden, haben Sie ein Kennwort zum Schützen der Datenbank und ein weiteres Kennwort zum Verschlüsseln der Datenbank. Bei Datenbanken der Version Access 2007 (.accdb) und höher (.mdb) können Sie die Datenbank nur mit einem Kennwort verschlüsseln und schützen, da die Option zur Verwendung von zwei verschiedenen Kennwörtern entfernt wurde.</span><span class="sxs-lookup"><span data-stu-id="1353f-p113">Encrypted passwords are dependent on the file format of the database that you are using. If you are using an Access 2003 (.mdb) or earlier database, you will have one password to protect the database, and a separate password to encrypt the database. For Access 2007 (.accdb) and later (.mdb) databases, the only option is to encrypt and protect the database with one password, as the option to have two separate passwords has been removed.</span></span>

> [!NOTE]
> <span data-ttu-id="1353f-247">Für Access 2007-Datenbanken (ACCDB) ist das Kennwort der Verschlüsselungsschlüssel.</span><span class="sxs-lookup"><span data-stu-id="1353f-247">For Access 2007 (.accdb) databases, the password is the encryption key</span></span>

<span data-ttu-id="1353f-248">Sie können den folgenden VBA-Beispielcode für eine Befehlsschaltfläche verwenden:</span><span class="sxs-lookup"><span data-stu-id="1353f-248">You can use the following example VBA code for a command button:</span></span>

```vb
    Private Sub Command0_Click()
    
    Dim strSourcePath As String
    Dim strDestPath As String
    
    strSourcePath = "<path>\sourceDb.accdb"
    strDestPath = "<path>\destDb.accdb"
    
    DBEngine.CompactDatabase strSourcePath, strDestPath, dbLangGeneral & ";pwd=Access", dbVersion120, ";pwd=Access"
    
    Set CurrentDatabase = CurrentDb
    Set LinkedTableDef = CurrentDatabase.CreateTableDef 
    ("My Linked Table")
    LinkedTableDef.Connect = "MS Access;pwd=Access";database=" & strDestPath
    LinkedTableDef.RefreshLink
    
    
    MsgBox "Finished"
    
    End Sub 
```

<br/>

<span data-ttu-id="1353f-249">Das folgende Codebeispiel veranschaulicht, wie CompactDatabase mit einem Kennwort (Schlüssel) verwenden, und klicken Sie dann auf eine Tabelle in die komprimierte Datenbank verknüpfen.</span><span class="sxs-lookup"><span data-stu-id="1353f-249">The following code sample shows how to use CompactDatabase with a password (encryption key) and then link to a table in that compacted database.</span></span> <span data-ttu-id="1353f-250">Beachten Sie, dass ein Kennwort eingegeben werden muss.</span><span class="sxs-lookup"><span data-stu-id="1353f-250">Note that a password must be supplied.</span></span>

```vb
    Private Sub CompactAndLink_Click() 
     
    Dim strSourcePath As String
    Dim strDestPath As String
    Dim strSourceTableName As String
    Dim strDestTableName As String
    Dim tdf As TableDef
     
    strSourcePath = "<path>\<database>.accdb"
    strDestPath = "<path>\<database>.accdb"
    strSourceTableName = "<table name in destination database>"
    strDestTableName = "<linked table name>"
     
    ' Compact source database into new destination database with encrypted password
    DBEngine.CompactDatabase strSourcePath, strDestPath, dbLangGeneral & ";pwd=Access", dbVersion120, ";pwd=Access"
     
    ' Link to one of the tables in the destination database
    ' Password must be provided in the Connect property
     
    Set CurrentDatabase = CurrentDb
    Set tdf = CurrentDatabase.CreateTableDef(strDestTableName)
       
        With tdf
            .Connect = ";pwd=Access" & ";DATABASE=" & strDestPath
            .SourceTableName = strSourceTableName
        End With
        
    CurrentDatabase.TableDefs.Append tdf
     
    MsgBox "Database compacted and encrypted password applied. Link to table also completed."
     
    End Sub
```
