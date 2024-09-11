export const goalComplitions = pgTable('goal_completions', {
  id: text('id').primaryKey(),
  goalId: text('goal_id')
    .references(() => goals.id)
    .notNull(),
  createdAt: timestamp('created_at', { withTimezone: true })
  .defaultNow()
  .notNull(),
})
