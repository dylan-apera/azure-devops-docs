---
title: Manage your product and portfolio backlogs with Azure Boards
titleSuffix: Azure Boards
description: Learn how to work with a hierarchical team structure to manage product and portfolio backlogs and to track progress across teams.
ms.technology: devops-agile
ms.assetid: F6FF6E6B-C9AA-4681-9205-D48C8F29D94B  
ms.author: kaelli
author: KathrynEE
ms.topic: tutorial
monikerRange: '<= azure-devops'
ms.date: 10/20/2021
---

# Use Azure Boards to manage your product and portfolio backlogs 

[!INCLUDE [version-lt-eq-azure-devops](../../includes/version-lt-eq-azure-devops.md)]

Portfolio backlogs provide product owners insight into the work done by several agile feature teams. Product owners can define the high-level goals as Epics or Features. Feature teams can break down these work items into the user stories they'll prioritize and develop.  

In this article you'll learn:  

>[!div class="checklist"]    
> * How to support a management view of multiple team progress
> * How feature teams can focus on their team backlog progress  
> * How to assign work from a common backlog
> * How to set up a hierarchical set of teams and backlogs

[!INCLUDE [configure-customize](../includes/note-configure-customize.md)]

By setting up a team structure like the one shown, you provide each feature team with their distinct backlog to plan, prioritize, and track their work. And, portfolio or product owners can create their vision, roadmap, and goals for each release, monitor progress across their portfolio of projects, and manage risks and dependencies.  

![Each team has its own view of the work](media/pm-team-structure.png) 

[Set up a hierarchical team and backlog structure](configure-hierarchical-teams.md) when you want to support the following elements:

- Autonomous feature teams that can organize and manage their backlog of work
- Portfolio management views for planning epics and features and monitoring progress of subordinate feature teams
- Assign backlog items to feature teams from a common backlog 

[!INCLUDE [image differences](../includes/image-differences.md)]

## Management view of team progress 

In this example, we show the **Epics** portfolio backlog for the **Management** team. Drilling down, you can see all the backlog items and features, even though they belong to one of three different teams: Customer Service, Phone, and Web.  

::: moniker range=">= azure-devops-2019"

> [!div class="mx-imgBorder"]  
> ![Backlog that shows parents and multi-team ownership.](../backlogs/media/multi-ownership/management-team-backlog-epics.png)   

::: moniker-end


::: moniker range=">= tfs-2017 <= tfs-2018"

In this example, we show the **Epics** portfolio backlog for the **Management** team. Drilling down, you can see all the backlog items and features, even though they belong to one of three different teams: Customer Service, Phone, and Web.   

> [!div class="mx-imgBorder"]  
> ![Backlog that shows parents and multi-team ownership.](../backlogs/media/multi-ownership/management-team-backlog-epics-pre-nav.png)

::: moniker-end

::: moniker range="<= tfs-2015"

The Fabrikam Account Management portfolio owner has several campaigns to start and deliver in the coming year. The owner creates an epic for each campaign and then breaks down each epic into various features that contribute to each campaign. 

With the hierarchical structure implemented, portfolio owners working in Account Management can view the epic, feature, and product backlogs for their area. 

<img src="media/pm-account-management-backlog-view.png" alt="Epic backlog of account management team" /> 

All work items under the Fabrikam/Account Management area path appear in their backlog view. You can expand a single item or use the expand ![expand icon](../media/icons/expand_icon.png) and collapse ![collapse icon](../media/icons/collapse_icon.png) icons to expand or collapse one level of the hierarchy. 

::: moniker-end


::: moniker range=">= tfs-2017 <= tfs-2018"

> [!TIP]    
> Program managers can also gain insight into progress across teams using [Delivery plans](review-team-plans.md). See also [Visibility across teams](visibility-across-teams.md).  

::: moniker-end


<a id="feature-team-backlog"> </a>

## Feature team backlog ownership and view of progress 

Each feature team has its own team home page or dashboards, product and portfolio backlogs, Kanban boards, and taskboards. These pages only show work relevant to each team. The relevance is based on assignments made to the work item area and iteration paths. For details, see [About teams and Agile tools](../../organizations/settings/about-teams-and-settings.md).

> [!TIP]
> Add **Node Name** to the column options to show the team assigned to the work item.   

::: moniker range=">= azure-devops-2019"

The Customer Service feature team's view of the backlog only includes those work items assigned to their area path, **Fabrikam Fiber/Customer Service**. Here we show parents that provide a few of the features and epics to which the backlog items belong. Items that are owned by other teams appear with hollow-filled bars. For example, Mobile feedback and Text alerts belong to the Account Management team. 

Items that are owned by other teams appear with an information icon,  :::image type="icon" source="../../media/icons/info.png" border="false"::: .

> [!div class="mx-imgBorder"]  
> ![Backlog that shows parents and multi-team ownership](../backlogs/media/multi-ownership/customer-service-backlog-parents-on.png)   

::: moniker-end


::: moniker range=">= tfs-2017 <= tfs-2018"

Items that are owned by other teams appear with an information icon,  :::image type="icon" source="../../media/icons/info.png" border="false"::: . 

> [!div class="mx-imgBorder"]  
> ![Backlog that shows parents and multi-team ownership](../backlogs/media/multi-ownership/customer-service-backlog-parents-on-prev-nav.png)   

::: moniker-end

::: moniker range="tfs-2017"

Backlog displays with work item icons is supported for TFS 2017.2 and later versions. For TFS 2017.1 and earlier versions, items that are owned by other teams appear with hollow-filled bars.  

<img src="../backlogs/media/ALM_OB_CustServTeamBacklog.png" alt="Team backlog is filtered based on area path ownership" /> 

::: moniker-end

::: moniker range="<= tfs-2015"

The Customer Profile feature team's view of the backlog only includes those work items assigned to their area path, **Fabrikam/Account Management/Customer Profile**. Here we show parents that provide a few of the features and epics to which the backlog items belong. Items that are owned by other teams appear with hollow-filled bars. For example, Mobile feedback and Text alerts belong to the Account Management team.   

<img src="media/pm-customer-profile-backlog-view.png" alt="Backlog view of Customer profile feature team" /> 

::: moniker-end

 
## Assign work from a common backlog

While the hierarchical team and backlog structure works well to support autonomous teams to take ownership of their backlog, it also supports assigning work to teams from a common backlog. During a sprint or product planning meeting, product owners and development leads can review the backlog. Teams can also assign select items to various teams by assigning them to the feature team Area Path. 

In this view of the Account Management backlog, all items still assigned to **Account Management** have yet to be assigned.

::: moniker range=">= azure-devops-2019" 

> [!div class="mx-imgBorder"]  
> ![Management team common backlog](media/portfolio/account-management-backlog.png) 

During the planning meeting, you can open each item, make notes, and assign the item to the team to work on it. 

> [!TIP]
> You can multi-select work items and perform a bulk edit of the area path. See [Bulk modify work items](../backlogs/bulk-modify-work-items.md).    

Here, all backlog items have been assigned to feature teams while all features and epics remain owned by Account Management. 

> [!div class="mx-imgBorder"]  
> ![All backlog items have been assigned to feature teams.](media/portfolio/account-management-backlog-assigned.png) 

::: moniker-end


::: moniker range=">= tfs-2017 <= tfs-2018"

In this view of the Account Management backlog, all items still assigned to **Account Management** have yet to be assigned.

> [!div class="mx-imgBorder"]  
> ![Management team common backlog](media/portfolio/account-management-backlog-prev-nav.png) 

During the planning meeting, you can open each item, make notes, and assign the item to the team to work on it. 

> [!TIP]    
> You can multi-select work items and perform a bulk edit of the area path. See [Bulk modify work items](../backlogs/bulk-modify-work-items.md).    

Here, all backlog items have been assigned to feature teams while all features and epics remain owned by Account Management. 

> [!div class="mx-imgBorder"]  
> ![All backlog items have been assigned to feature teams.](media/portfolio/account-management-backlog-assigned.png) 

::: moniker-end

::: moniker range="<= tfs-2015"

In this view of the Account Management backlog, all items still assigned to **Account Management** have yet to be assigned.

<img src="media/pm-assign-items-from-common-backlog.png" alt="Backlog view-Assign items from a common backlog" /> 

During the planning meeting, you can open each item, make notes, and assign the item to the team to work on it. 

Here, all backlog items have been assigned to feature teams while all features and epics remain owned by Account Management. 

<img src="media/pm-items-assigned-from-common-backlog.png" alt="Backlog view-Items assigned from a common backlog" />

::: moniker-end


## Add portfolio backlogs 

::: moniker range=">= azure-devops-2019"

If you need more than three backlog levels, you can add more. To learn how, see [Customize your backlogs or boards for a process](../../organizations/settings/work/customize-process-backlogs-boards.md). 

::: moniker-end
 
::: moniker range="<= tfs-2018"

If you need more than three backlog levels, you can add more. To learn how, see [Add portfolio backlogs](../../reference/add-portfolio-backlogs.md).

::: moniker-end

## Track dependencies across teams 

The simplest way to track dependencies across teams is to link work items using the **Related** link type. If they're dependent in time, then you can use the **Predecessor/Successor** link types.  You can then create queries that find work items containing these relationships. See [Manage dependencies, link work items to support traceability](../queries/link-work-items-support-traceability.md) to learn more. 
  
::: moniker range="azure-devops"
Using Delivery Plans, you can track dependencies across projects within an organization. To learn more, see [Track dependencies using Delivery Plans](../plans/track-dependencies.md). 

To track dependencies across organizations, see [Plan and track dependencies using the Dependency Tracker](../extensions/dependency-tracker.md). 
::: moniker-end

::: moniker range="< azure-devops"
To track dependencies across organizations, see [Plan and track dependencies using the Dependency Tracker](../extensions/dependency-tracker.md). 
::: moniker-end

::: moniker range=">= tfs-2017"

## Portfolio feature progress

::: moniker-end

::: moniker range=">= azure-devops-2020"

To view feature progress based on linked requirements, you can add a rollup column or view the Feature Timeline. To learn more, see [Display rollup](../backlogs/display-rollup.md) and [View portfolio progress with the Feature Timeline](../extensions/feature-timeline.md). 

::: moniker-end

::: moniker range=">= tfs-2017 < azure-devops"

To view feature progress based on linked requirements, you can view the Feature Timeline. To learn more, see [View portfolio progress with the Feature Timeline](../extensions/feature-timeline.md). 

::: moniker-end


## Try this next

> [!div class="nextstepaction"]
> [Configure a hierarchy of teams](configure-hierarchical-teams.md)


## Related articles
 
- [Create your backlog](../backlogs/create-your-backlog.md)  
- [Kanban quickstart](../boards/kanban-quickstart.md)
- [Assign work to sprints](../sprints/assign-work-sprint.md)
- [Organize your backlog](../backlogs/organize-backlog.md)
- [Limitations of multi-team Kanban board views](../boards/kanban-overview.md#limits-multi-team)




 