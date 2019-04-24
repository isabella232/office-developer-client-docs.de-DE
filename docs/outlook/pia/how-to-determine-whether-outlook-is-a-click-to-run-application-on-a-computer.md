---
title: Bestimmen, ob Outlook eine Klick-und-Los-Anwendung auf einem Computer ist
TOCTitle: Determine whether Outlook is a Click-to-Run application on a computer
ms:assetid: 1b8573be-8ea8-4973-869d-87fda57ce525
ms:mtpsurl: https://msdn.microsoft.com/library/Ff522355(v=office.15)
ms:contentKeyID: 55119804
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 4a710baa4d70ac69b67d2a06fe694998884fd835
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32356406"
---
# <a name="determine-whether-outlook-is-a-click-to-run-application-on-a-computer"></a><span data-ttu-id="74c74-102">Bestimmen, ob Outlook eine Klick-und-Los-Anwendung auf einem Computer ist</span><span class="sxs-lookup"><span data-stu-id="74c74-102">Determine whether Outlook is a Click-to-Run application on a computer</span></span>

<span data-ttu-id="74c74-103">Klick-und-Los ist in Office 2010 und höheres Versionen eine Möglichkeit zur Bereitstellung und Aktualisierung von Software.</span><span class="sxs-lookup"><span data-stu-id="74c74-103">Click-to-Run is a software delivery and updating mechanism available to Office 2010 and later versions.</span></span> <span data-ttu-id="74c74-104">Produkte, die über Klick-und-Los bereitgestellt werden, werden in einer virtuellen Umgebung auf dem lokalen Betriebssystem ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="74c74-104">Products delivered via Click-to-Run execute in a virtual application environment on the local operating system.</span></span> <span data-ttu-id="74c74-105">Dies bedeutet, dass diese Produkte über private Kopien ihrer Dateien und Einstellungen verfügen und sämtliche erfolgten Änderungen in der virtuellen Umgebung erfasst werden.</span><span class="sxs-lookup"><span data-stu-id="74c74-105">This means that they have private copies of their files and settings, and that any changes they make are captured in the virtual environment.</span></span>

<span data-ttu-id="74c74-106">Klick-und-Los ist schnell – Benutzer können innerhalb kürzester Zeit mit dem Ausführen einer Anwendung beginnen, ohne warten zu müssen, bis das ganze Produkt installiert wurde.</span><span class="sxs-lookup"><span data-stu-id="74c74-106">Click-to-Run is fast—users can start running an application within a short time without waiting for the complete product to finish installing.</span></span> <span data-ttu-id="74c74-107">Updates werden automatisch im Hintergrund ausgeführt, ohne dass ein Benutzerzuerst eine Installation entfernen oder Updates manuell installieren muss.</span><span class="sxs-lookup"><span data-stu-id="74c74-107">Updates are run automatically in the background, without requiring a user to first remove an installation or manually install updates.</span></span> <span data-ttu-id="74c74-108">Klick-und-Los-Produkte sind virtualisiert und stehen nicht im Konflikt mit anderer installierter Software.</span><span class="sxs-lookup"><span data-stu-id="74c74-108">Click-to-Run products are virtualized and do not conflict with other installed software.</span></span> <span data-ttu-id="74c74-109">Da ein Produkt, das über Klick-und-Los bereitgestellt wurde, aber über private Kopien aller Dateien und der Registrierung verfügt, kann der Add-In-Entwickler nicht in gleicher Weise über das Vorhandensein des Produkts bestimmen, wie dies bei einem Produkt der Fall ist, das auf der Festplatte des Clientcomputers installiert wurde.</span><span class="sxs-lookup"><span data-stu-id="74c74-109">However, because a product delivered by Click-to-Run has private copies of all its files and registration, an add-in developer cannot determine the product’s existence in the same manner as a product that was installed on a client computer’s hard disk.</span></span> <span data-ttu-id="74c74-110">Ab Outlook 2010 sollten Add-In-Entwickler überprüfen, ob Outlook installiert wurde und ob Outlook als Klick-und-Los-Produkt bereitgestellt wurde.</span><span class="sxs-lookup"><span data-stu-id="74c74-110">Starting with Outlook 2010, add-in developers should verify whether Outlook has been installed, and whether Outlook has been delivered as a Click-to-Run product.</span></span>


> [!NOTE]
> <span data-ttu-id="74c74-111">In der virtuellen Klick-und-Los-Anwendungsumgebung wird nur 32-Bit-Office 2013 unterstützt, auch wenn der Clientcomputer über ein 64-Bit-Betriebssystem verfügt.</span><span class="sxs-lookup"><span data-stu-id="74c74-111">Only 32-bit Office 2013 is supported in the Click-to-Run virtual application environment, even if the client computer runs a 64-bit operating system.</span></span>



### <a name="to-check-whether-outlook-2013-was-delivered-by-click-to-run-on-a-client-computer"></a><span data-ttu-id="74c74-112">So prüfen Sie, ob Outlook 2013 per Klick-und-Los auf dem Clientcomputer bereitgestellt wurde</span><span class="sxs-lookup"><span data-stu-id="74c74-112">To check whether Outlook 2013 was delivered by Click-to-Run on a client computer</span></span>

- <span data-ttu-id="74c74-113">Überprüfen Sie, ob der VirtualOutlook-Schlüssel am folgenden Speicherort in der Windows-Registrierung vorhanden ist:</span><span class="sxs-lookup"><span data-stu-id="74c74-113">Verify whether the VirtualOutlook key exists in the following location in the Windows registry:</span></span>
    
  `HKEY_LOCAL_MACHINE\SOFTWARE\WOW6432Node\Microsoft\Office\15.0\Common\InstallRoot\Virtual\VirtualOutlook`
    
  <span data-ttu-id="74c74-114">Der Schlüssel VirtualOutlook ist ein REG\_SZ-Wert mit dem Gebietsschemakennzeichen des installierten Produkts, z. B. "en-us".</span><span class="sxs-lookup"><span data-stu-id="74c74-114">The VirtualOutlook key is a REG\_SZ value that contains the culture tag of the installed product language, such as "en-us".</span></span>

## <a name="see-also"></a><span data-ttu-id="74c74-115">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="74c74-115">See also</span></span>

- [<span data-ttu-id="74c74-116">Add-In-Verwaltung</span><span class="sxs-lookup"><span data-stu-id="74c74-116">Add-in administration</span></span>](add-in-administration.md)

