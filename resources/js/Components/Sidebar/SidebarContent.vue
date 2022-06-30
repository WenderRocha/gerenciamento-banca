<template>
  <PerfectScrollbar
    tagname="nav"
    aria-label="main"
    class="relative flex flex-col flex-1 max-h-full gap-4 px-3"
  >
    <SidebarLink
      title="Gerênciamento"
      :href="route('dashboard')"
      :active="route().current('dashboard')"
    >
      <template #icon>
        <DashboardIcon class="flex-shrink-0 w-6 h-6" aria-hidden="true" />
      </template>
    </SidebarLink>

      <SidebarLink
      title="Desempenho"
      :href="route('analysis.index')"
      :active="route().current('analysis')"
    >
      <template #icon>
        <AnalysisIcon class="flex-shrink-0 w-6 h-6" aria-hidden="true" />
      </template>
    </SidebarLink>

    <SidebarLink
      title="Carteiras"
      :href="route('wallet.index')"
      :active="route().current('wallet')"
    >
      <template #icon>
        <WalletsIcon class="flex-shrink-0 w-6 h-6" aria-hidden="true" />
      </template>
    </SidebarLink>

    <SidebarLink
      title="Transações"
      :href="route('transaction.index')"
      :active="route().current('transaction')"
    >
      <template #icon>
        <TransactionIcon class="flex-shrink-0 w-6 h-6" aria-hidden="true" />
      </template>
    </SidebarLink>

    <SidebarLink
      title="Trades"
      :href="route('trade.index')"
      :active="route().current('trades')"
    >
      <template #icon>
        <TradesIcon class="flex-shrink-0 w-6 h-6" aria-hidden="true" />
      </template>
    </SidebarLink>

    <SidebarLink
      title="Book Trade"
      :href="route('book.index')"
      :active="route().current('book')"
    >
      <template #icon>
        <BookIcon class="flex-shrink-0 w-6 h-6" aria-hidden="true" />
      </template>
    </SidebarLink>

    <SidebarLink
      title="Suporte"
      :href="route('support.index')"
      :active="route().current('support')"
    >
      <template #icon>
        <SupportIcon class="flex-shrink-0 w-6 h-6" aria-hidden="true" />
      </template>
    </SidebarLink>

    <SidebarCollapsible
      title="Ferramentas"
      :active="route().current('components.*')"
    >
      <template #icon>
        <CogIcon class="flex-shrink-0 w-6 h-6" aria-hidden="true" />
      </template>

      <SidebarCollapsibleItem
        :href="route('components.buttons')"
        title="Buttons"
        :active="route().current('components.buttons')"
      />
    </SidebarCollapsible>

    <SidebarCollapsible
      title="Administração"
      :active="route().current('components.*')"
    >
      <template #icon>
        <SecureIcon class="flex-shrink-0 w-6 h-6" aria-hidden="true" />
      </template>

      <SidebarCollapsibleItem
        :href="route('components.buttons')"
        title="Usuarios"
        :active="route().current('components.buttons')"
      />

      <SidebarCollapsibleItem
        :href="route('components.buttons')"
        title="Planos"
        :active="route().current('components.buttons')"
      />

      <SidebarCollapsibleItem
        :href="route('components.buttons')"
        title="Assinantes"
        :active="route().current('components.buttons')"
      />
    </SidebarCollapsible>

    <SidebarLink
      title="Suporte"
      :href="route('support.index')"
      :active="route().current('support')"
    >
      <template #icon>
        <DashboardIcon class="flex-shrink-0 w-6 h-6" aria-hidden="true" />
      </template>
    </SidebarLink>

    <!-- Examples -->
    <!-- 
        => External link example
        <SidebarLink
            title="Github"
            href="https://github.com/kamona-wd/kui-laravel-breeze"
            external
            target="_blank"
        >
        </SidebarLink>

        => Collapsible examples
        <SidebarCollapsible title="Users" :active="$page.url.startsWith('/users')">
            <SidebarCollapsibleItem :href="route('users.index')" title="List" :active="$page.url === '/users/index'" />
            <SidebarCollapsibleItem :href="route('users.create')" title="Create" :active="$page.url === '/users/create'" />
        </SidebarCollapsible>

        <SidebarCollapsible title="Users" :active="usePage().url.value.startsWith('/users')">
            <template #icon>
                <UserIcon
                    class="flex-shrink-0 w-6 h-6"
                    aria-hidden="true"
                />
            </template>

            <SidebarCollapsibleItem :href="route('users.index')" title="List" :active="route().current('users.index')" />
            <SidebarCollapsibleItem :href="route('users.create')" title="Create" :active="route().current('users.create')" />
        </SidebarCollapsible>-->
  </PerfectScrollbar>
</template>

<script setup>
import PerfectScrollbar from "@/Components/PerfectScrollbar";
import SidebarLink from "@/Components/Sidebar/SidebarLink";

import {
  DashboardIcon,
  SecureIcon,
  CogIcon,
  WalletsIcon,
  TransactionIcon,
  TradesIcon,
  BookIcon,
  SupportIcon,
  AnalysisIcon
} from "@/Components/Icons/outline";

import SidebarCollapsible from "@/Components/Sidebar/SidebarCollapsible";
import SidebarCollapsibleItem from "@/Components/Sidebar/SidebarCollapsibleItem";
import { TemplateIcon } from "@heroicons/vue/outline";
import { FigmaIcon } from "@/Components/Icons/brands";
</script>
