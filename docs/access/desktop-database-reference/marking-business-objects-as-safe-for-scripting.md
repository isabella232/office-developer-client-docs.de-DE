---
title: Kennzeichnen von Geschäftsobjekten als sicher für die Verwendung von Skript
TOCTitle: Marking Business Objects as Safe for Scripting
ms:assetid: 8ee49aec-672d-96f7-baa6-9261317a4d90
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249630(v=office.15)
ms:contentKeyID: 48546295
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 195e9fc25e3aa8871233ebe60441d29909b31a48
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "25878311"
---
# <a name="marking-business-objects-as-safe-for-scripting"></a><span data-ttu-id="2408b-102">Kennzeichnen von Geschäftsobjekten als sicher für die Verwendung von Skript</span><span class="sxs-lookup"><span data-stu-id="2408b-102">Marking Business Objects as Safe for Scripting</span></span>


<span data-ttu-id="2408b-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="2408b-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="2408b-p101">Sie müssen jedes Geschäftsobjekt, das mit der [CreateObject](dataspace-object-rds.md)-Methode des [RDS.DataSpace](createobject-method-rds.md)-Objekts instanziiert wird, als "Sicher für Skripts" kennzeichnen, um eine möglichst sichere Internetumgebung zu erreichen. Vergewissern Sie sich, dass die Objekte im Lizenzbereich der Systemregistrierung entsprechend gekennzeichnet sind, damit sie in DCOM verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="2408b-p101">To help ensure a secure Internet environment, you need to mark any business objects instantiated with the [RDS.DataSpace](dataspace-object-rds.md) object's [CreateObject](createobject-method-rds.md) method as "safe for scripting." You need to ensure they are marked as such in the License area of the system registry before they can be used in DCOM.</span></span>

<span data-ttu-id="2408b-p102">Wenn Sie ein Geschäftsobjekt manuell als sicher für Skript kennzeichnen möchten, erstellen Sie eine Textdatei mit der Erweiterung REG, die den folgenden Text enthält. Mit den folgenden beiden Nummern wird das Feature für eine sichere Verwendung von Skript aktiviert:</span><span class="sxs-lookup"><span data-stu-id="2408b-p102">To manually mark your business object as safe for scripting, create a text file with a .reg extension that contains the following text. The following two numbers enable the safe-for-scripting feature:</span></span>

```vb 
 
[HKEY_CLASSES_ROOT\CLSID\<MyActiveXGUID>\Implemented 
Categories\{7DD95801-9882-11CF-9FA9-00AA006C42C4}] 
[HKEY_CLASSES_ROOT\CLSID\<MyActiveXGUID>\Implemented 
Categories\{7DD95802-9882-11CF-9FA9-00AA006C42C4}] 
```

<span data-ttu-id="2408b-108">wobei \< *MyActiveXGUID* \> hexadezimale GUID-Nummer des Geschäftsobjekts ist.</span><span class="sxs-lookup"><span data-stu-id="2408b-108">where \<*MyActiveXGUID*\> is the hexadecimal GUID number of your business object.</span></span> <span data-ttu-id="2408b-109">Speichern Sie es, und in der Registrierung durch den Registrierungs-Editor verwenden oder durch Doppelklicken auf die REG-Datei in Windows Explorer zusammengeführt.</span><span class="sxs-lookup"><span data-stu-id="2408b-109">Save it and merge it into your registry by using the Registry Editor or double-clicking the .reg file in Windows Explorer.</span></span>

<span data-ttu-id="2408b-p104">Geschäftsobjekte, die in Microsoft® Visual Basic erstellt werden, können mit dem Paket- und Bereitstellungs-Assistenten automatisch als "sicher für Skript" gekennzeichnet werden. Wählen Sie **Safe for initialization** und **Safe for scripting** aus, wenn Sie vom Assistenten auffordert werden, Sicherheitseinstellungen anzugeben.</span><span class="sxs-lookup"><span data-stu-id="2408b-p104">Business objects created in Microsoft® Visual Basic can be automatically marked as "safe for scripting" with the Package and Deployment Wizard. When the wizard asks you to specify safety settings, select **Safe for initialization** and **Safe for scripting**.</span></span>

<span data-ttu-id="2408b-p105">Im letzten Schritt erstellt der Anwendungseinrichtungs-Assistent eine HTM- und eine CAB-Datei. Sie können diese beiden Dateien anschließend auf den Zielcomputer kopieren. Doppelklicken Sie dann auf die HTM-Datei, um die Seite zu laden und den Server ordnungsgemäß zu registrieren.</span><span class="sxs-lookup"><span data-stu-id="2408b-p105">On the last step, the Application Setup Wizard creates an .htm and a .cab file. You can then copy these two files to the target computer and double-click the .htm file to load the page and correctly register the server.</span></span>

<span data-ttu-id="2408b-114">Da das Geschäftsobjekt, das in der Windows installiert wird\\System32\\Occache Verzeichnis standardmäßig auf die Fenster verschieben\\Ordner System32, und ändern Sie die **HKEY\_Klassen\_ROOT\\CLSID\\ \*\* \< *MyActiveXGUID*\>\\**InprocServer32\*\* Registrierungsschlüssel, der den richtigen Pfad entspricht.</span><span class="sxs-lookup"><span data-stu-id="2408b-114">Because the business object will be installed in the Windows\\System32\\Occache directory by default, move it to the Windows\\System32 directory and change the **HKEY\_CLASSES\_ROOT\\CLSID\\**\<*MyActiveXGUID*\>\\**InprocServer32** registry key to match the correct path.</span></span>


> [!NOTE]
> <span data-ttu-id="2408b-p106">[!HINWEIS] Geschäftsobjekte, die für die Verwendung von Skript oder für die Initialisierung als sicher gekennzeichnet sind, können von jedem Benutzer über das Netzwerk instanziiert und initialisiert werden. Benutzerdefinierte Geschäftsobjekte dürfen nicht unbedacht entworfen und implementiert werden. Es ist absolut notwendig, dass diese Objekte kein Sicherheitsrisiko darstellen und Hacker durch sie keinen Zugriff auf den vertraulichen Bereich des Hostservers erlangen und Schaden verursachen können.</span><span class="sxs-lookup"><span data-stu-id="2408b-p106">Business objects marked as safe for scripting or safe for initialization can be instantiated and initialized by anyone over the network. Any custom business object must not be designed and implemented casually. It is imperative that such objects do not present a security threat that hackers can explore to gain access to the sensitive area of the hosting server and inflict damages.</span></span>


